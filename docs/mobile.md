---
layout: page
title: Mobile Application Manual
permalink: /mobile
---

# Mobile Application

## Índice
- [Mobile Application](#mobile-application)
  - [Índice](#índice)
  - [General](#general)
  - [Instalación](#instalación)
  - [Landing](#landing)
  - [Signup](#signup)
    - [Email y contraseña](#email-y-contraseña)
    - [Cliente federado (Facebook)](#cliente-federado-facebook)
  - [Login](#login)
    - [Email y Contraseña](#email-y-contraseña-1)
    - [Federado (Facebook)](#federado-facebook)
    - [Login Datos biométricos](#login-datos-biométricos)
    - [Post Login](#post-login)


## General

La aplicación de SnapMsg fue desarrollada con React Native, solo para funcionar en dispositivos Android. Esta estuvo probada con la version 33 del SDK de Android.

## Instalación

Para instalar el apk primero se debe descargar el .apk desde la (fuente)[https://expo.dev//accounts/monsech/projects/7552-snapmsg-mobileapp/builds/a3438543-d2ad-44fa-a689-f0956267d0a9]

Una vez descargado, hay que instalarlo via USB, seguir el siguiente (tutorial)[https://es.wikihow.com/instalar-archivos-APK-de-una-PC-en-Android], una vez instalado se puede inicializar desde el icono.

## Landing

Cuando se levanta la aplicación lo primero que se visualiza es la vista de Landing donde se muestran las opciones para crear cuenta, loguear en la aplicación (por email, federada y biometrico) y la recuperación de contraseña.

<img src="./docs/assets/images/mobile/landing.jpg" height="450">

## Signup

Existen 2 maneras de crear una cuenta nueva:
  - Con email y contraseña
  - Con cliente federado (Facebook)

### Email y contraseña

Al ingresar a la opción de `sign up for snapmsg` se llevará al formulario de creación de cuenta, donde se le solicitarán al usuario datos requeridos para la creación de cuenta, el mismo validará que los datos cumplan con los requerimientos cuando se intente enviar el formulario

<img src="./docs/assets/images/mobile/register_empty.jpg" height="450">
<img src="./docs/assets/images/mobile/register_validation.jpg" height="450">
<img src="./docs/assets/images/mobile/register_complete.jpg" height="450">

Una vez aprobada la creación de la cuenta, se notificará al usuario con un mensaje de que la misma debe ser verificada al email especificado en el formulario que contendrá las instrucciones para su verificación.

<img src="./docs/assets/images/mobile/register_validation_info.jpg" height="450">
 
Cuando el usuario siga las instrucciones provistas en el email, podrá validar su cuenta y así loguearse a la plataforma.

### Cliente federado (Facebook)

Para utilizar tu cuenta de Facebook puedes continuar al boton de Facebook donde se pedirá que confirmes que apruebas a FB a autenticar con Snapmsg

<img src="./docs/assets/images/mobile/facebook_confirmation.jpg" height="450">

En este modo de creación de cuenta, no hace falta verificarlo por email, dado que Snapmsg esta utilizando el servicio de Fb.


## Login

Existen 3 maneras diferentes métodos loguear con la aplicación:
  - Login con email y contraseña
  - Login federado usando Facebook
  - Login con datos biométricos: aunque este requiere cualquiera de los dos anteriores, dado que puede activarse una vez que la cuenta exista

### Email y Contraseña

Cuando se intente loguear se visualizará el formulario de login donde se pedirá email y contraseña de la cuenta previamente creada.

<img src="./docs/assets/images/mobile/login_empty.jpg" height="450">

El mismo validará que las credenciales sean válidas, notificando al usuario si estas no lo son.

<img src="./docs/assets/images/mobile/login_invalid.jpg" height="450">

### Federado (Facebook)

El proceso para login con facebook es el mismo que para la creación de cuenta, internamente Snapmsg verifica que se haya logueado al menos una vez con Facebook para crear la cuenta de SnapMsg, pero las subsecuentes veces directamente hará login

### Login Datos biométricos

Esta opción debe ser configurada desde la edición de perfil, si esta fue configurada exitosamente, entonces cuando se aprete el boton de la huella digital, pedirá los datos biométricos del usuario (huella, patrón, foto frontal) para validar al usuario, si estos datos son correctos, entonces procederá al login a la plataforma.

### Post Login

Aprobado el login, este puede dirigir a dos lugares diferentes dependiendo de la situación

1. Si es la primera vez que se loguea (despues de crear la cuenta), entonces Snapmsg pedirá que completes un formulario de Onboarding para conocerte un poco más y personalizar tu experiencia con los demás usuarios, una vez completados estos pasos, que son requeridos para comenzar a usar Snapmsg, el onboarding te llevará al feed de Snapmsg.
Si el usuario no completa el proceso de onboarding el mismo lo volverá a llevar al primer paso de Onboarding para completarlo
2. Si el usuario ya hizo onboarding previo, entonces irá directamente al Feed




