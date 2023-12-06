---
layout: page
title: Backoffice Manual
permalink: /backoffice
---

# Backoffice

## Índice
- [Backoffice](#backoffice)
  - [Índice](#índice)
  - [General ](#general-)
  - [Login](#login)
  - [Layout](#layout)
    - [Navbar](#navbar)
    - [Sidebar](#sidebar)
  - [Dashboards](#dashboards)
  - [Perfil](#perfil)
  - [Usuarios](#usuarios)
    - [Bloquear usuario](#bloquear-usuario)
    - [Visualizar Usuario](#visualizar-usuario)
  - [Perfil del Usuario](#perfil-del-usuario)
  - [Verificación de cuenta](#verificación-de-cuenta)
  - [Verificación de cuenta detalle](#verificación-de-cuenta-detalle)
  - [Snaps](#snaps)
  - [Detalle Snap](#detalle-snap)
  - [Servicios](#servicios)
  - [Servicio Detalle](#servicio-detalle)
  - [Alta Administradores](#alta-administradores)

## General <a name="general"></a>
Para acceder al portal de administradores de SnapMsg se debe dar acceso a través del meta administrador. Este le indicará a su dirección de email el acceso a la [plataforma](https://7552-snapmsg-backoffice.vercel.app/l)

## Login
El acceso a la platforma iniciará con la siguiente vista donde se deberá introducir los datos.

<img src="./docs/assets/images/login.png" width="450">

## Layout

La plataforma de administrador provee una layout compuesta por 3 elementos importantes

- Navbar
- Sidebar
- Contenido

### Navbar
En la parte superior se podra visualizar con la navbar, en la cual se permitirá desplegar la sidebar con todas las acciones posibles del administrador y también podra visualizar acceder a su cuenta y desloguearse de la herramienta.

<img src="./docs/assets/images/navbar.png" width="450">

### Sidebar

Desde la sidebar se podrán acceder a todas las acciones que pueden realizar los administradores

<img src="./docs/assets/images/sidebar-closed.png" width="130">
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
<img src="./docs/assets/images/sidebar-open.png" width="200">



## Dashboards

Una vez ingresada a la plataforma se podrán acceder a los dashboards de usuarios y contenidos (snaps), accediendo a cada uno a través de las tabs.

<img src="./docs/assets/images/users_dashboard.png" width="450">

<img src="./docs/assets/images/content_dashboard.png" width="450">

Ambos dasboards tienen sus controles internos para filtrar por fecha o para cambiar alguna configuracion

## Perfil

La plataforma permite modificar los datos del administrador, al interactuar con el boton edit, el formulario permitira la modificación para aquellos campos que admitan modificación.

<img src="./docs/assets/images/perfil.png" width="450">


## Usuarios

Se podran visualizar todos los usuarios creados en snapmsg, estos seran visibles desde una tabla donde se muestran algunas características de los usuarios junto con la posibilidad de visualizar su perfil en detalle y la opción de bloquear y desbloquearlo de usar la aplicación.

<img src="./docs/assets/images/users_grid.png" width="450">

### Bloquear usuario

Se podrá bloquear y desbloquear usuario si se hace click al icon de bloqueo, este estara indicado con color verde si el usuario puede usar la aplicación y estara marcado en rojo si el usuario se encuentra bloqueado

Cuando se interactúe con este botón, se pedirá confirmación por parte del administrador si desea ejecutar la acción deseada.

<img src="./docs/assets/images/users_block_prompt.png" width="450">

Una vez que la acción haya sido aprobada, habrá una notificación confirmando o rechazando la acción, así también como la actualización del color del botón y de la medalla.

<img src="./docs/assets/images/users_block_confirmation.png" width="450">


### Visualizar Usuario

Desde el botón con el ojo, se podrá ir al detalle de visualización de perfil del usuario.

## Perfil del Usuario

En la vista de visualización de perfil se podrán ver todos las propiedades de ese usuario con toda los datos del mismo actualizados en su ultima interacción con snapmsg.

<img src="./docs/assets/images/user_profile.png" width="450">

Aca se indicará el estado del mismo en la plataforma (si se encuentra bloqueado) junto con su foto de perfil, cantidad de likes, cantidad de shares, etc.

## Verificación de cuenta

Los usuarios de snapmsg pueden validar su cuenta con la plataforma, para indicar al resto de los usuarios que son quienes dicen ser. Para esto hay un portal de verificación de cuentas, donde los administradores podrán ver todas las peticiones pendientes, aprobadas y rechazadas de los usuarios que hayan solicitado verificar su perfil.

Desde la vista de verificación de cuenta, se mostrarán en primer lugar todas las solicitudes pendientes, pero también utilizando las tabs, se podrán visualizar las aprobadas y rechazadas.

<img src="./docs/assets/images/verifications_grid.png" width="450">

La única acción realizable sobre cada una de las verificaciónes (pendientes, aprobadas y rechazadas) sera ir al detalle de la misma.

## Verificación de cuenta detalle

A los administradores se les pedirá como condición necesaria para validar la cuenta, que revisen dos fotos que los usuarios subirán a través de la aplicación, estas fotos son del fronto del documento de identidad y una selfie para poder acreditar con la foto del documento de identidad.

Ambas fotos pueden visualizarse completas si se interactúa con las cards de las previsualizaciones de las fotos.
Finalmente el administrador tendrá la potestad de aprobar o rechazar la solicitud del usuario, en donde se le pedirá conrfirmación al hacerlo y se notificará con el éxito o rechazo de la acción.


<img src="./docs/assets/images/verification_prompt.png" width="450">

<img src="./docs/assets/images/verification_success.png" width="450">

## Snaps

El elemento central de la plataforma son los Snaps, por esto desde el sistema de administradores, podrán visualizarse todos los snaps que fueron creados por los usuarios de SnapMsg. Estos como los usuarios podrán ser pre visualizados en formato de tabla, donde también se podrá ir al detalle del Snap, o inclusive bloquearlo si no cumple con el código de conducta o desbloquearlo.

<img src="./docs/assets/images/snaps_grid.png" width="450">

Así mismo como en el caso de los usuarios, se pedirá confirmación para bloquear y desbloquear y se indicará con una notificación y actualizacón de la data en tiempo real el exito o rechazo de la acción

<img src="./docs/assets/images/block_snap.png" width="450">

<img src="./docs/assets/images/snap_block_confirmation.png" width="450">

## Detalle Snap

Desde la vista de detalle del Snap seleccionado desde la vista anterior, se podrá acceder a todos los datos de ese Snap especifico, como la metadata propia del snap y los resultados de las interacciones que tuvo con los demas usuarios.

<img src="./docs/assets/images/snap_detail.png" width="450">

## Servicios

Como administrador es importante velar por la salud de los servicios que son consumidos por la aplicación mobile, por esto hay una sección dedicada a estos, donde se podrán ver todos los servicios que dispone SnapMsg en formato de tabla. Desde aquí se podrá ir al detalle del servicio, para poder realizar chequeos de salud del mismo así también como ver información de ese servicio en particular y también se podrá acceder a la documentación de la api del mismo (si es que esta disponible).

<img src="./docs/assets/images/services_grid.png" width="450">

En la tabla se dará como resúmen el estado del servicio y cuando fue que se reviso por última vez.

## Servicio Detalle

Desde el detalle del servicio, será posible visualizar la información asociada al servicio y se podrán ejecutar pruebas para validar su estado de salud, haciendo click en el boton de run check.

<img src="./docs/assets/images/service_detail.png" width="450">

Al hacer click en el botón se ejecutará una prueba en tiempo real, validando el estado del servicio. si El mismo se encuentra caído indicará con un DOWN y si esta activo con OK. También se actualizará cuando se reviso por última vez. Recomendamos realizar estos chequeos de manera cotidiana.

<img src="./docs/assets/images/service_check.png" width="450">

La tabla también permanecerá actualizada con los resultados de la última prueba corrida.

<img src="./docs/assets/images/serice_check_after.png" width="450">

## Alta Administradores

Desde la plataforma, se podrá dar de alta nuevos administradores a través del formulario de alta, ahi se deberá ingresar los datos del admin para que este sea dado de alta en el sistema. Este no requiere verificación.

<img src="./docs/assets/images/new_admin.png" width="450">

Cuando se cree el nuevo usuario se recibira una confirmación para notificar que la creación fue exitosa.

<img src="./docs/assets/images/new_admin_confirmation.png" width="450">

Desde el boton de logout podrá salir de la plataforma.