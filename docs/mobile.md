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
    - [Pre login](#pre-login)
    - [Email y Contraseña](#email-y-contraseña-1)
    - [Federado (Facebook)](#federado-facebook)
    - [Login Datos biométricos](#login-datos-biométricos)
    - [Post Login](#post-login)
  - [Recuperación de contraseña](#recuperación-de-contraseña)
  - [Feed](#feed)
    - [Favorite Snaps](#favorite-snaps)
    - [Notifications Center](#notifications-center)
    - [Creacion de un snap](#creacion-de-un-snap)
  - [Busqueda](#busqueda)
    - [Busqueda por texto o hashtag](#busqueda-por-texto-o-hashtag)
  - [Lista de mensajes](#lista-de-mensajes)
    - [Chat](#chat)
  - [Perfil de usuario](#perfil-de-usuario)
    - [Perfil de usuario propio](#perfil-de-usuario-propio)
    - [Verificación de usuario](#verificacion-de-usuario)
    - [Estadisticas de snaps](#estadisticas-de-snaps)
    - [Edición de perfil](#edicion-de-perfil)
    - [Perfil de usuario ajeno](#perfil-de-usuario-ajeno)


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

### Pre login

Si la cuenta fue creada con email y contraseña y esta no fue verificada con las instrucciones enviadas por email, SnapMsg le avisará al usuario que todavía su cuenta no fue verificada y le da la posibilidad de volver a envíar las instrucciones

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

## Recuperación de contraseña

Snapmsg permite la recuperación de contraseña mediante el formulario desde la vista de login, este pedirá que el usuario ingrese su email, para que se le envién las instrucciones de reseteo de contraseña vía email.

<img src="./docs/assets/images/mobile/forgot_password.jpg" height="450">

Este indicará con éxito cuando las instrucciones hayan sido enviadas.

<img src="./docs/assets/images/mobile/password_reset_confirmation.jpg" height="450">

## Feed

Luego de iniciar sesión, se ingresa al home de la aplicación, donde se podrá navegar dentro de la misma. En la pestaña de feed podemos ver un listado de Snaps que cumplen con al menos uno de los siguientes criterios

1. Snaps publicados por mi
2. Snaps publicados por usuarios que sigo
3. Snaps reposteador por usuarios que sigo, o por mi
4. Snaps que podrian interesarme de usuarios que no sigo pero con los cuales comparto intereses

Desde la vista de feed se puede ademas acceder a los snaps guardados como favoritos, al centro de notificaciones o crear un nuevo snap.

<img src="./docs/assets/images/mobile/feed.png" height="450">

### Favorite Snaps

Si un snap me interesa y tiene información que no quiero perder o lo quiero tener a mano, lo puedo agregar a favoritos con el simbolo de un marcador de libros, el cual se pondrá amarillo luego de apretarlo.

De esta manera, si accedemos a los snaps favoritos podemos ver un listado con todos los snaps que agregué previamente a favoritos, y podemos sacarlo simplemente apretando nuevamente en el simbolo amarillo del mismo.

<img src="./docs/assets/images/mobile/favorite_snaps.png" height="450">

### Notifications Center

En el centro de notificaciones podremos ver todas las notificaciones que nos llegaron a nuestra cuenta por nuevos seguidores, por mensajes de amigos, o por interacciones de otros usuarios con nuestras publicaciones, como podria ser likes, reposts, o menciones en sus propias publicaciones.

Si se presiona una notificacion sucederá una de las siguientes situaciones:

1. Nos llevará al perfil del usuario que nos comenzó a seguir
2. Nos llevará al chat con el usuario que nos envión un mensaje
3. Nos llevará al snap en el cual nos mencionaron, o al cual le dieron like/repost

<img src="./docs/assets/images/mobile/notifications_center.png" height="450">

### Creacion de un snap

Desde acá podemos crear un snap con el texto que queremos, el sistema tiene un limite de caracteres, por lo que no nos permitirá publicarlo si no tiene al menos un caracter o si tiene mas de 140.

Para evitar estos problemas, tenemos un contador que nos dice cuantos caracteres vamos escribiendo, y el color del boton para publicar cambiará cuando se nos permita publicar.

Además, tenemos la opción de seleccionar si queremos que nuestro snap sea privado o publico con la casilla que dice 'Private snap'

<img src="./docs/assets/images/mobile/new_snap.png" height="450">

## Busqueda

Cuando vamos a la pestaña de busqueda podemos encontrar información de distintas formas. En la parte superior tenemos una barra de busqueda donde podrmeos buscar usuarios o snaps a traves de texto o un hashtag. Cuando se escribe una busqueda suceden simultaneamente varias cosas:

1. Se ofrece al usuario un hashtag que coincide con el texto escrito, para buscar snaps que tengan ese hashtag. En el ejemplo a continuación el usuario busca 'el' y se puede ver la opcion '#el'. Si se presiona esta opción se procederá a la busqueda de snaps por hashtag.
2. Se muestran todos los usuarios que contengan la busqueda en su nombre de usuario o nombre de perfil. Si se presiona uno de ellos, se dirige al perfil seleccionado.
3. Si no se encuentran usuarios con la busqueda provista, entonces se hace saber mediante el mensaje 'No users matching: (la busqueda)'

Una vez que el usuario terminó de escribir puede presionar enter en el teclado o la lupita de la barra para buscar snaps por texto o hashtag

Por ultimo, se muestra al final de la vista un carrusel con usuarios recomendados para seguir, con distintos criterios: se tiene en cuenta la cantidad de intereses en común con estos usuarios, y la distancia a la que se encuentran. A estos usuarios se los puede seguir o se puede visitar su perfil.

<img src="./docs/assets/images/mobile/busqueda.png" height="450">
<img src="./docs/assets/images/mobile/busqueda_sin_resultados.png" height="450">

### Busqueda por texto o hashtag

Cuando el usuario realiza la busqueda, podrá ver los snaps que incluyan el texto elegido, o el hashtag elegido. En los ejemplos, se realiza una busqueda con el texto 'Hola', luego una busqueda con hashtag '#TanBionica' y por ultimo una busqueda que no tiene resultados.

<img src="./docs/assets/images/mobile/busqueda_texto.png" height="450">
<img src="./docs/assets/images/mobile/busqueda_hashtag.png" height="450">
<img src="./docs/assets/images/mobile/busqueda_texto_sin_resultados.png" height="450">

## Lista de mensajes

En esta pestaña se pueden ver una lista de todos los chats y conversaciones que iniciamos con otros usuarios.

En caso de no tener conversaciones se verá simplemente un mensaje que indica que no tenemos conversaciones, pero en caso de ya haber chateado con otros usuarios, lo veremos listado, con la información del otro usuario, el tiempo desde que se envió el ultimo mensaje y el texto del ultimo mensaje. Y si presionamos en una tarjeta podremos acceder al chat con esa persona para seguir conversando.

<img src="./docs/assets/images/mobile/messages_list_empty.png" height="450">
<img src="./docs/assets/images/mobile/messages_list.png" height="450">

### Chat

Cuando ingresamos a un chat podemos ver el nombre del usuario con el que estamos conversando, y todos los mensajes que se enviaron entre los usuarios. A la izquierda y con color lila se verán los enviados por el otro usuario, y a la derecha con color gris los enviados por nosotros mismos.

<img src="./docs/assets/images/mobile/chat.png" height="450">

## Perfil de usuario

En la barra de navegacion podemos ir a la pestaña del perfil, donde inicialmente nos encontraremos con nuestro perfil, pero desde donde podremos acceder a distintas opciones como se verá a continuación

### Perfil de usuario propio

En la vista de nuestro perfil tenemos 3 secciones:

1. Nuestra información personal como nombre, usuario, mail y nuestra foto de perfil. Además tendremos una insignia que nos indicará si nuestro perfil está verificado o no.
2. Una sección de botones que nos permiten acceder a estadisticas de nuestros snaps, a la edición de nuestros datos, o cerrar nuestra sesión.
3. La cantidad de seguidos y seguidores, que nos permite acceder a una lista de los usuarios que seguimos o nos siguen.
4. Una vista de todos nuestros snaps publicados o reposteados. La misma se divide en dos pestañas, una que contiene todos nuestros snaps publicados y reposteados, y otra que nos muestra unicamente nuestros snaps reposteados.

<img src="./docs/assets/images/mobile/user_profile.png" height="450">

### Verificación de usuario

Si tocamos la insignia en nuestro perfil, SnapMsg nos permite solicitar la verificación de nuestro usuario. Cuando ingresamos a esta sección se nos explica el proceso a través del cual debemos enviar fotos de nuestro documento de identificación, del frente y el dorso, y un administrador de SnapMsg nos aceptará o rechazará el pedido.

Si el pedido es aceptdo podremos ver en nuestro perfil una insignia para que todos los usuarios sepan que fuimos verificados.

<img src="./docs/assets/images/mobile/verify_account.png" height="450">

### Estadisticas de snaps

Cuandos se accede a esta sección se pueden ver estadisticas de snaps en distintos rangos de fechas, pudiendo elegir entre los ultimos 7 dias, las ultimas 2 semanas, el ultimo mes, los ultimos 3 meses, 6 meses o el ultimo año.

Las estadisticas que se podrán ver son:

1. La cantidad de snaps publicados
2. La cantidad de likes dados a otros snaps
3. La cantidad de shares recibidos a snaps
4. La cantidad de comentarios que recibieron mis snaps

<img src="./docs/assets/images/mobile/snaps_statistics.png" height="450">

### Edición de perfil

En esta sección podremos ver los datos que ingresamos al momento de registrarnos, y podremos modificar solo algunos de ellos. 

Entre los datos que se pueden modificar se encuentran la foto de perfil, pudiendose sacar una foto o elegir de la galeria, el nombre a mostrar, el genero y la fecha de nacimiento, siempre cumpliendo que sea un usuario mayor de edad.

Entre los datos que no se pueden modificar se encuentra el email de registro y el nombre de usuario.

Por ultimo desde esta sección podemos tambien habilitar el ingreso a la aplicación con datos biometricos, y se le solicitará permiso al usuario del telefono.

<img src="./docs/assets/images/mobile/edit_profile_1.png" height="450">
<img src="./docs/assets/images/mobile/edit_profile_2.png" height="450">

### Perfil de usuario ajeno

Por ultimo, podemos acceder de distintas formas al perfil de otro usuario de la plataforma, ya sea a través de un snap que publicó, a través de las recomendaciones de cuentas o de la busqueda de usuarios.

En esta sección veremos información similar a la de nuestro propio perfil pero con menos opciones, ya que no veremos información privada del usuario como su email, y no podremos acceder a las estadisticas de sus snaps.

En este caso tendremos la opcion de seguir al usuario (o dejar de seguirlo si corresponde), o de iniciar un chat con el mismo, como ya se vio en la sección de lista de mensajes.

<img src="./docs/assets/images/mobile/other_user_profile.png" height="450">
