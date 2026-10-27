# CAPÍTULO III: REQUIREMENTS SPECIFICATION
## 3.1. User Stories

### Epics

Los siguientes Epics agrupan las User Stories y Technical Stories de biciGO según las principales capacidades funcionales del sistema.

<table border="1" cellspacing="0" cellpadding="7" style="border-collapse: collapse; width: 100%; border: 2px solid black;">
  <tr>
    <th align="center">Epic ID</th>
    <th align="center">Título</th>
    <th align="center">Descripción</th>
    <th align="center">Historias relacionadas</th>
  </tr>
  <tr>
    <td valign="top"><b>EP-01</b></td>
    <td valign="top">Gestión de cuentas y autenticación</td>
    <td valign="top">Agrupa las funcionalidades relacionadas con el registro, inicio de sesión, verificación, recuperación de contraseña y seguridad de acceso de los usuarios en biciGO.</td>
    <td valign="top">US-01 a US-05, TS-01 a TS-04</td>
  </tr>
  <tr>
    <td valign="top"><b>EP-02</b></td>
    <td valign="top">Localización y disponibilidad de bicicletas</td>
    <td valign="top">Incluye las funcionalidades que permiten consultar la ubicación, disponibilidad, información y cobertura de las bicicletas dentro de las zonas donde opera biciGO.</td>
    <td valign="top">US-06 a US-10, US-39, TS-05 a TS-07</td>
  </tr>
  <tr>
    <td valign="top"><b>EP-03</b></td>
    <td valign="top">Gestión de alquileres y viajes</td>
    <td valign="top">Reúne las funcionalidades necesarias para iniciar, desbloquear, consultar y finalizar alquileres, así como controlar la información del recorrido y su costo.</td>
    <td valign="top">US-11 a US-15, TS-08 a TS-11</td>
  </tr>
  <tr>
    <td valign="top"><b>EP-04</b></td>
    <td valign="top">Pagos, tarifas y suscripciones</td>
    <td valign="top">Comprende la gestión de métodos de pago, tarifas, cobros, comprobantes y planes de suscripción para usuarios frecuentes de biciGO.</td>
    <td valign="top">US-16 a US-20, US-36, US-37, TS-12 a TS-14</td>
  </tr>
  <tr>
    <td valign="top"><b>EP-05</b></td>
    <td valign="top">Perfil, historial y gestión personal</td>
    <td valign="top">Agrupa las funcionalidades que permiten al usuario consultar y actualizar su perfil, revisar viajes anteriores, gestionar su contraseña y desactivar su cuenta.</td>
    <td valign="top">US-21 a US-25, US-40, TS-15 y TS-16</td>
  </tr>
  <tr>
    <td valign="top"><b>EP-06</b></td>
    <td valign="top">Incidencias, soporte y notificaciones</td>
    <td valign="top">Incluye el reporte y seguimiento de problemas, la comunicación con soporte y la gestión de notificaciones relacionadas con alquileres, pagos e incidencias.</td>
    <td valign="top">US-26 a US-30, US-38, TS-17 y TS-18</td>
  </tr>
  <tr>
    <td valign="top"><b>EP-07</b></td>
    <td valign="top">Administración y gestión operativa</td>
    <td valign="top">Reúne las funcionalidades administrativas necesarias para supervisar la flota, gestionar usuarios e incidencias y consultar métricas operativas del servicio.</td>
    <td valign="top">US-31 a US-35, TS-19 y TS-20</td>
  </tr>
</table>


<table border="1" cellspacing="0" cellpadding="7" style="border-collapse: collapse; width: 100%; border: 2px solid black;">
    <tr>
      <th align="center">Epic / Story ID</th>
      <th align="center">Título</th>
      <th align="center">Descripción</th>
      <th align="center">Criterios de Aceptación</th>
      <th align="center">Relacionado con (Epic ID)</th>
    </tr>
    <tr>
      <td valign="top"><b>US-01</b></td>
      <td valign="top">Registro de usuario</td>
      <td valign="top"><b>Como visitante</b>, quiero registrarme en biciGO proporcionando mis datos personales y credenciales, para poder acceder a los servicios de alquiler de bicicletas.</td>
      <td valign="top"><b>Escenario 1: Registro exitoso</b><br><br><b>Given</b> que el visitante no posee una cuenta registrada<br><b>When</b> completa todos los campos obligatorios con información válida<br><b>Then</b> el sistema crea la cuenta correctamente<br><b>And</b> permite al usuario acceder a la plataforma.<br><br><b>Escenario 2: Correo electrónico ya registrado</b><br><br><b>Given</b> que existe una cuenta asociada al correo proporcionado<br><b>When</b> el visitante intenta registrarse utilizando dicho correo<br><b>Then</b> el sistema rechaza el registro<br><b>And</b> informa que el correo ya se encuentra registrado.<br><br><b>Escenario 3: Datos obligatorios incompletos</b><br><br><b>Given</b> que el visitante se encuentra en el formulario de registro<br><b>When</b> intenta registrarse sin completar todos los campos obligatorios<br><b>Then</b> el sistema no crea la cuenta<br><b>And</b> indica qué información debe completar.</td>
      <td valign="top"><b>EP-01</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-02</b></td>
      <td valign="top">Inicio de sesión</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero iniciar sesión con mis credenciales, para acceder de forma segura a las funcionalidades de biciGO.</td>
      <td valign="top"><b>Escenario 1: Inicio de sesión exitoso</b><br><br><b>Given</b> que el usuario posee una cuenta activa<br><b>When</b> ingresa un correo electrónico y una contraseña válidos<br><b>Then</b> el sistema autentica al usuario<br><b>And</b> permite acceder a la pantalla principal.<br><br><b>Escenario 2: Contraseña incorrecta</b><br><br><b>Given</b> que el correo pertenece a una cuenta registrada<br><b>When</b> el usuario proporciona una contraseña incorrecta<br><b>Then</b> el sistema rechaza el acceso<br><b>And</b> informa que las credenciales son incorrectas.<br><br><b>Escenario 3: Cuenta inexistente</b><br><br><b>Given</b> que el usuario se encuentra en la pantalla de inicio de sesión<br><b>When</b> proporciona un correo no registrado<br><b>Then</b> el sistema no inicia sesión<br><b>And</b> informa que no existe una cuenta asociada al correo.</td>
      <td valign="top"><b>EP-01</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-03</b></td>
      <td valign="top">Recuperación de contraseña</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero recuperar el acceso a mi cuenta cuando olvide mi contraseña, para poder continuar utilizando biciGO.</td>
      <td valign="top"><b>Escenario 1: Solicitud válida</b><br><br><b>Given</b> que el usuario posee una cuenta registrada<br><b>When</b> solicita recuperar su contraseña utilizando su correo<br><b>Then</b> el sistema inicia el proceso de recuperación<br><b>And</b> envía las instrucciones correspondientes.<br><br><b>Escenario 2: Correo no registrado</b><br><br><b>Given</b> que el usuario se encuentra en la opción de recuperación de contraseña<br><b>When</b> ingresa un correo no asociado a ninguna cuenta<br><b>Then</b> el sistema no inicia el proceso<br><b>And</b> informa que el correo no está registrado.<br><br><b>Escenario 3: Nueva contraseña válida</b><br><br><b>Given</b> que el usuario accedió correctamente al proceso de recuperación<br><b>When</b> establece una nueva contraseña que cumple los requisitos<br><b>Then</b> el sistema actualiza sus credenciales<br><b>And</b> permite iniciar sesión con la nueva contraseña.</td>
      <td valign="top"><b>EP-01</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-04</b></td>
      <td valign="top">Verificación de cuenta</td>
      <td valign="top"><b>Como usuario recién registrado</b>, quiero verificar mi cuenta, para confirmar mis datos y habilitar el acceso completo a los servicios de biciGO.</td>
      <td valign="top"><b>Escenario 1: Verificación exitosa</b><br><br><b>Given</b> que el usuario posee una cuenta pendiente de verificación<br><b>When</b> realiza correctamente el proceso de validación<br><b>Then</b> el sistema marca la cuenta como verificada<br><b>And</b> habilita las funcionalidades correspondientes.<br><br><b>Escenario 2: Verificación inválida</b><br><br><b>Given</b> que el usuario intenta validar su cuenta<br><b>When</b> utiliza información o un código de verificación inválido<br><b>Then</b> el sistema rechaza la verificación<br><b>And</b> solicita realizar nuevamente el proceso.<br><br><b>Escenario 3: Cuenta previamente verificada</b><br><br><b>Given</b> que la cuenta ya fue verificada<br><b>When</b> el usuario intenta repetir el proceso<br><b>Then</b> el sistema mantiene el estado de la cuenta<br><b>And</b> informa que la verificación ya fue realizada.</td>
      <td valign="top"><b>EP-01</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-05</b></td>
      <td valign="top">Cierre de sesión</td>
      <td valign="top"><b>Como usuario autenticado</b>, quiero cerrar mi sesión, para evitar que otras personas accedan a mi cuenta desde el mismo dispositivo.</td>
      <td valign="top"><b>Escenario 1: Cierre exitoso</b><br><br><b>Given</b> que el usuario mantiene una sesión activa<br><b>When</b> selecciona la opción de cerrar sesión<br><b>Then</b> el sistema finaliza la sesión<br><b>And</b> redirige al usuario a la pantalla de acceso.<br><br><b>Escenario 2: Acceso posterior al cierre</b><br><br><b>Given</b> que la sesión fue finalizada<br><b>When</b> el usuario intenta acceder a una funcionalidad restringida<br><b>Then</b> el sistema bloquea el acceso<br><b>And</b> solicita iniciar sesión nuevamente.<br><br><b>Escenario 3: Sesión expirada</b><br><br><b>Given</b> que la sesión del usuario ha expirado<br><b>When</b> intenta realizar una operación protegida<br><b>Then</b> el sistema impide continuar<br><b>And</b> solicita nuevamente sus credenciales.</td>
      <td valign="top"><b>EP-01</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-06</b></td>
      <td valign="top">Permitir acceso a ubicación</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero permitir que biciGO acceda a mi ubicación, para identificar bicicletas disponibles cercanas.</td>
      <td valign="top"><b>Escenario 1: Permiso concedido</b><br><br><b>Given</b> que el usuario accede por primera vez al mapa<br><b>When</b> concede permiso para utilizar su ubicación<br><b>Then</b> el sistema obtiene su ubicación aproximada<br><b>And</b> centra el mapa en la zona correspondiente.<br><br><b>Escenario 2: Permiso rechazado</b><br><br><b>Given</b> que el sistema solicita acceso a la ubicación<br><b>When</b> el usuario rechaza el permiso<br><b>Then</b> la plataforma continúa funcionando<br><b>And</b> permite consultar manualmente otras zonas.<br><br><b>Escenario 3: Ubicación no disponible</b><br><br><b>Given</b> que el usuario permitió el acceso a su ubicación<br><b>When</b> el dispositivo no puede determinarla<br><b>Then</b> el sistema informa la situación<br><b>And</b> permite buscar una ubicación manualmente.</td>
      <td valign="top"><b>EP-02</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-07</b></td>
      <td valign="top">Visualización de bicicletas cercanas</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero visualizar las bicicletas disponibles cerca de mi ubicación, para elegir una alternativa conveniente para mi viaje.</td>
      <td valign="top"><b>Escenario 1: Bicicletas disponibles</b><br><br><b>Given</b> que existen bicicletas disponibles cerca del usuario<br><b>When</b> accede al mapa principal<br><b>Then</b> el sistema muestra las bicicletas disponibles<br><b>And</b> indica su ubicación aproximada.<br><br><b>Escenario 2: Sin bicicletas disponibles</b><br><br><b>Given</b> que no existen bicicletas disponibles en la zona consultada<br><b>When</b> el usuario visualiza el mapa<br><b>Then</b> el sistema informa que no existen unidades disponibles<br><b>And</b> mantiene visible el mapa para consultar otras zonas.<br><br><b>Escenario 3: Cambio de disponibilidad</b><br><br><b>Given</b> que una bicicleta cambia de estado<br><b>When</b> el usuario actualiza la información del mapa<br><b>Then</b> el sistema refleja el nuevo estado<br><b>And</b> evita mostrar información obsoleta.</td>
      <td valign="top"><b>EP-02</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-08</b></td>
      <td valign="top">Consulta de información de bicicleta</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero consultar la información de una bicicleta, para verificar su disponibilidad y condición antes de alquilarla.</td>
      <td valign="top"><b>Escenario 1: Consulta exitosa</b><br><br><b>Given</b> que el usuario observa una bicicleta en el mapa<br><b>When</b> selecciona dicha bicicleta<br><b>Then</b> el sistema muestra su información disponible<br><b>And</b> indica si puede ser alquilada.<br><br><b>Escenario 2: Bicicleta no disponible</b><br><br><b>Given</b> que la bicicleta seleccionada dejó de estar disponible<br><b>When</b> el usuario consulta su información<br><b>Then</b> el sistema muestra su estado actualizado<br><b>And</b> impide iniciar un alquiler.<br><br><b>Escenario 3: Bicicleta fuera de servicio</b><br><br><b>Given</b> que una bicicleta fue marcada para mantenimiento<br><b>When</b> el usuario intenta consultarla para alquilarla<br><b>Then</b> el sistema informa que se encuentra fuera de servicio<br><b>And</b> no permite seleccionarla para alquiler.</td>
      <td valign="top"><b>EP-02</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-09</b></td>
      <td valign="top">Búsqueda de bicicletas por zona</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero buscar bicicletas en una zona específica, para planificar un desplazamiento aunque no me encuentre actualmente en ese lugar.</td>
      <td valign="top"><b>Escenario 1: Zona encontrada</b><br><br><b>Given</b> que el usuario desea consultar otra ubicación<br><b>When</b> ingresa una zona válida<br><b>Then</b> el sistema posiciona el mapa en esa zona<br><b>And</b> muestra las bicicletas disponibles.<br><br><b>Escenario 2: Zona sin disponibilidad</b><br><br><b>Given</b> que la ubicación ingresada es válida<br><b>When</b> no existen bicicletas disponibles en ella<br><b>Then</b> el sistema informa que no existen unidades disponibles.<br><br><b>Escenario 3: Ubicación inválida</b><br><br><b>Given</b> que el usuario utiliza el buscador<br><b>When</b> ingresa una ubicación que no puede ser identificada<br><b>Then</b> el sistema informa que la ubicación no fue encontrada<br><b>And</b> permite realizar una nueva búsqueda.</td>
      <td valign="top"><b>EP-02</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-10</b></td>
      <td valign="top">Actualización de disponibilidad</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero actualizar la disponibilidad de bicicletas mostrada, para consultar información reciente antes de seleccionar una unidad.</td>
      <td valign="top"><b>Escenario 1: Actualización exitosa</b><br><br><b>Given</b> que el usuario se encuentra visualizando el mapa<br><b>When</b> solicita actualizar la información<br><b>Then</b> el sistema obtiene los estados más recientes<br><b>And</b> actualiza las bicicletas mostradas.<br><br><b>Escenario 2: Bicicleta recientemente ocupada</b><br><br><b>Given</b> que una bicicleta estaba disponible anteriormente<br><b>When</b> otro usuario inicia su alquiler<br><b>Then</b> el sistema actualiza su estado<br><b>And</b> deja de mostrarla como disponible.<br><br><b>Escenario 3: Error al actualizar</b><br><br><b>Given</b> que existe un problema de comunicación<br><b>When</b> el usuario solicita actualizar el mapa<br><b>Then</b> el sistema informa que no pudo obtener datos recientes<br><b>And</b> permite intentar nuevamente.</td>
      <td valign="top"><b>EP-02</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-11</b></td>
      <td valign="top">Inicio de alquiler</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero iniciar el alquiler de una bicicleta disponible, para utilizarla durante mi desplazamiento.</td>
      <td valign="top"><b>Escenario 1: Inicio exitoso</b><br><br><b>Given</b> que el usuario se encuentra autenticado y la bicicleta está disponible<br><b>When</b> solicita iniciar el alquiler<br><b>Then</b> el sistema registra el inicio del servicio<br><b>And</b> asigna la bicicleta al usuario.<br><br><b>Escenario 2: Bicicleta no disponible</b><br><br><b>Given</b> que la bicicleta seleccionada ya está siendo utilizada<br><b>When</b> el usuario intenta alquilarla<br><b>Then</b> el sistema rechaza la solicitud<br><b>And</b> informa que la bicicleta no está disponible.<br><br><b>Escenario 3: Alquiler previamente activo</b><br><br><b>Given</b> que el usuario ya posee un alquiler activo<br><b>When</b> intenta iniciar otro alquiler<br><b>Then</b> el sistema rechaza la operación<br><b>And</b> solicita finalizar primero el alquiler actual.</td>
      <td valign="top"><b>EP-03</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-12</b></td>
      <td valign="top">Desbloqueo de bicicleta</td>
      <td valign="top"><b>Como usuario con un alquiler autorizado</b>, quiero desbloquear la bicicleta mediante el mecanismo proporcionado por biciGO, para comenzar mi recorrido.</td>
      <td valign="top"><b>Escenario 1: Desbloqueo exitoso</b><br><br><b>Given</b> que existe un alquiler válido asociado a la bicicleta<br><b>When</b> el usuario utiliza correctamente el código de desbloqueo<br><b>Then</b> el sistema autoriza el desbloqueo<br><b>And</b> habilita el inicio del recorrido.<br><br><b>Escenario 2: Código incorrecto</b><br><br><b>Given</b> que el usuario intenta desbloquear una bicicleta<br><b>When</b> introduce un código inválido<br><b>Then</b> el sistema rechaza la operación<br><b>And</b> informa que el código no es válido.<br><br><b>Escenario 3: Código asociado a otra bicicleta</b><br><br><b>Given</b> que el usuario posee un alquiler activo<br><b>When</b> intenta utilizar el código en una bicicleta diferente<br><b>Then</b> el sistema impide el desbloqueo<br><b>And</b> indica la bicicleta correspondiente.</td>
      <td valign="top"><b>EP-03</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-13</b></td>
      <td valign="top">Consulta del viaje activo</td>
      <td valign="top"><b>Como usuario con un alquiler activo</b>, quiero consultar la información de mi recorrido, para conocer el estado actual de mi viaje.</td>
      <td valign="top"><b>Escenario 1: Viaje activo</b><br><br><b>Given</b> que el usuario posee un alquiler en curso<br><b>When</b> accede al detalle del viaje<br><b>Then</b> el sistema muestra la información disponible del recorrido<br><b>And</b> mantiene visible el estado activo.<br><br><b>Escenario 2: Sin viaje activo</b><br><br><b>Given</b> que el usuario no posee un alquiler vigente<br><b>When</b> intenta consultar un viaje activo<br><b>Then</b> el sistema informa que actualmente no existe uno.<br><br><b>Escenario 3: Información actualizada</b><br><br><b>Given</b> que el recorrido continúa en ejecución<br><b>When</b> el usuario actualiza la pantalla<br><b>Then</b> el sistema presenta los datos más recientes del viaje.</td>
      <td valign="top"><b>EP-03</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-14</b></td>
      <td valign="top">Consulta de costo durante el viaje</td>
      <td valign="top"><b>Como usuario con un alquiler activo</b>, quiero consultar el costo acumulado del recorrido, para controlar cuánto estoy gastando mientras utilizo la bicicleta.</td>
      <td valign="top"><b>Escenario 1: Costo disponible</b><br><br><b>Given</b> que existe un alquiler activo<br><b>When</b> el usuario consulta la información del viaje<br><b>Then</b> el sistema calcula el costo acumulado<br><b>And</b> lo muestra al usuario.<br><br><b>Escenario 2: Actualización del recorrido</b><br><br><b>Given</b> que el usuario continúa desplazándose<br><b>When</b> aumenta la distancia registrada<br><b>Then</b> el sistema recalcula el costo correspondiente<br><b>And</b> muestra el nuevo importe acumulado.<br><br><b>Escenario 3: Error temporal de cálculo</b><br><br><b>Given</b> que no puede obtenerse temporalmente la información necesaria<br><b>When</b> el usuario consulta el costo<br><b>Then</b> el sistema informa que el cálculo no está disponible momentáneamente<br><b>And</b> permite actualizarlo posteriormente.</td>
      <td valign="top"><b>EP-03</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-15</b></td>
      <td valign="top">Finalización de alquiler</td>
      <td valign="top"><b>Como usuario con un alquiler activo</b>, quiero finalizar correctamente mi alquiler, para detener el cobro y liberar la bicicleta para otros usuarios.</td>
      <td valign="top"><b>Escenario 1: Finalización exitosa</b><br><br><b>Given</b> que el usuario posee un alquiler activo<br><b>When</b> solicita finalizarlo correctamente<br><b>Then</b> el sistema registra la hora de finalización<br><b>And</b> calcula el importe total correspondiente.<br><br><b>Escenario 2: Bicicleta liberada</b><br><br><b>Given</b> que el alquiler fue finalizado correctamente<br><b>When</b> el sistema confirma el cierre<br><b>Then</b> la bicicleta cambia a estado disponible<br><b>And</b> puede ser consultada por otros usuarios cuando corresponda.<br><br><b>Escenario 3: Error durante la finalización</b><br><br><b>Given</b> que existe un problema al procesar el cierre<br><b>When</b> el usuario intenta finalizar el alquiler<br><b>Then</b> el sistema informa que la operación no pudo completarse<br><b>And</b> evita registrar un cierre incorrecto.</td>
      <td valign="top"><b>EP-03</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-16</b></td>
      <td valign="top">Registro de método de pago</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero registrar un método de pago, para poder pagar los servicios utilizados en biciGO.</td>
      <td valign="top"><b>Escenario 1: Método válido</b><br><br><b>Given</b> que el usuario se encuentra gestionando sus métodos de pago<br><b>When</b> proporciona información válida<br><b>Then</b> el sistema registra el método correctamente<br><b>And</b> lo deja disponible para futuros cobros.<br><br><b>Escenario 2: Información inválida</b><br><br><b>Given</b> que el usuario intenta registrar un método de pago<br><b>When</b> proporciona información incorrecta o incompleta<br><b>Then</b> el sistema rechaza el registro<br><b>And</b> solicita corregir la información.<br><br><b>Escenario 3: Error en validación</b><br><br><b>Given</b> que el método de pago no puede ser validado<br><b>When</b> se intenta completar el registro<br><b>Then</b> el sistema no lo almacena como válido<br><b>And</b> informa el inconveniente.</td>
      <td valign="top"><b>EP-04</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-17</b></td>
      <td valign="top">Consulta de tarifa</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero consultar la tarifa aplicable al alquiler, para conocer las condiciones de cobro antes de utilizar una bicicleta.</td>
      <td valign="top"><b>Escenario 1: Tarifa disponible</b><br><br><b>Given</b> que el usuario consulta una bicicleta disponible<br><b>When</b> revisa las condiciones del servicio<br><b>Then</b> el sistema muestra la tarifa vigente.<br><br><b>Escenario 2: Usuario con suscripción</b><br><br><b>Given</b> que el usuario posee un plan activo<br><b>When</b> consulta la tarifa<br><b>Then</b> el sistema muestra las condiciones correspondientes a su plan.<br><br><b>Escenario 3: Cambio de tarifa</b><br><br><b>Given</b> que las condiciones de precio fueron actualizadas<br><b>When</b> el usuario consulta un nuevo alquiler<br><b>Then</b> el sistema presenta la tarifa vigente actualizada.</td>
      <td valign="top"><b>EP-04</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-18</b></td>
      <td valign="top">Pago del alquiler</td>
      <td valign="top"><b>Como usuario</b>, quiero pagar el importe generado por mi alquiler, para completar correctamente la transacción del servicio utilizado.</td>
      <td valign="top"><b>Escenario 1: Pago exitoso</b><br><br><b>Given</b> que el alquiler fue finalizado y existe un importe pendiente<br><b>When</b> el sistema procesa un método de pago válido<br><b>Then</b> registra el pago correctamente<br><b>And</b> marca la transacción como completada.<br><br><b>Escenario 2: Pago rechazado</b><br><br><b>Given</b> que existe un importe pendiente<br><b>When</b> el método de pago es rechazado<br><b>Then</b> el sistema registra el pago como pendiente<br><b>And</b> informa que debe utilizarse otro método.<br><br><b>Escenario 3: Reintento de pago</b><br><br><b>Given</b> que existe un pago pendiente<br><b>When</b> el usuario proporciona un método válido y vuelve a intentarlo<br><b>Then</b> el sistema procesa nuevamente la transacción<br><b>And</b> actualiza su estado si fue aprobada.</td>
      <td valign="top"><b>EP-04</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-19</b></td>
      <td valign="top">Suscripción a plan mensual</td>
      <td valign="top"><b>Como usuario frecuente</b>, quiero contratar un plan mensual de biciGO, para acceder a condiciones de uso más convenientes.</td>
      <td valign="top"><b>Escenario 1: Suscripción exitosa</b><br><br><b>Given</b> que el usuario no posee una suscripción activa<br><b>When</b> selecciona un plan disponible y completa el pago<br><b>Then</b> el sistema activa la suscripción<br><b>And</b> muestra su periodo de vigencia.<br><br><b>Escenario 2: Pago rechazado</b><br><br><b>Given</b> que el usuario intenta contratar un plan<br><b>When</b> el pago no puede ser procesado<br><b>Then</b> el sistema no activa la suscripción<br><b>And</b> informa el resultado al usuario.<br><br><b>Escenario 3: Suscripción ya activa</b><br><br><b>Given</b> que el usuario ya posee el mismo plan vigente<br><b>When</b> intenta contratarlo nuevamente<br><b>Then</b> el sistema evita generar una suscripción duplicada<br><b>And</b> muestra la información del plan actual.</td>
      <td valign="top"><b>EP-04</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-20</b></td>
      <td valign="top">Cancelación de suscripción</td>
      <td valign="top"><b>Como usuario suscrito</b>, quiero cancelar mi suscripción mensual, para evitar futuras renovaciones cuando ya no desee utilizar el plan.</td>
      <td valign="top"><b>Escenario 1: Cancelación exitosa</b><br><br><b>Given</b> que el usuario posee una suscripción activa<br><b>When</b> solicita cancelarla<br><b>Then</b> el sistema registra la cancelación<br><b>And</b> evita futuras renovaciones.<br><br><b>Escenario 2: Vigencia restante</b><br><br><b>Given</b> que el usuario cancela una suscripción antes de finalizar su periodo<br><b>When</b> la cancelación es confirmada<br><b>Then</b> el sistema conserva los beneficios hasta la fecha establecida<br><b>And</b> informa cuándo finalizarán.<br><br><b>Escenario 3: Sin suscripción activa</b><br><br><b>Given</b> que el usuario no posee una suscripción vigente<br><b>When</b> intenta cancelarla<br><b>Then</b> el sistema informa que no existe un plan activo.</td>
      <td valign="top"><b>EP-04</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-21</b></td>
      <td valign="top">Consulta de perfil</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero consultar la información de mi perfil, para verificar los datos asociados a mi cuenta.</td>
      <td valign="top"><b>Escenario 1: Consulta exitosa</b><br><br><b>Given</b> que el usuario se encuentra autenticado<br><b>When</b> accede a su perfil<br><b>Then</b> el sistema muestra la información registrada en su cuenta.<br><br><b>Escenario 2: Sesión inválida</b><br><br><b>Given</b> que la sesión dejó de ser válida<br><b>When</b> el usuario intenta acceder al perfil<br><b>Then</b> el sistema impide el acceso<br><b>And</b> solicita iniciar sesión nuevamente.<br><br><b>Escenario 3: Información actualizada</b><br><br><b>Given</b> que el usuario modificó previamente sus datos<br><b>When</b> consulta nuevamente el perfil<br><b>Then</b> el sistema muestra la información actualizada.</td>
      <td valign="top"><b>EP-05</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-22</b></td>
      <td valign="top">Edición de perfil</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero modificar mis datos personales, para mantener actualizada la información de mi cuenta.</td>
      <td valign="top"><b>Escenario 1: Actualización exitosa</b><br><br><b>Given</b> que el usuario accede a la edición de perfil<br><b>When</b> modifica sus datos utilizando información válida<br><b>Then</b> el sistema guarda los cambios<br><b>And</b> muestra la información actualizada.<br><br><b>Escenario 2: Información inválida</b><br><br><b>Given</b> que el usuario está modificando sus datos<br><b>When</b> proporciona información con un formato incorrecto<br><b>Then</b> el sistema rechaza los cambios<br><b>And</b> indica qué datos deben corregirse.<br><br><b>Escenario 3: Campos obligatorios vacíos</b><br><br><b>Given</b> que existen campos necesarios para mantener la cuenta<br><b>When</b> el usuario intenta dejarlos vacíos<br><b>Then</b> el sistema impide guardar los cambios<br><b>And</b> solicita completar la información requerida.</td>
      <td valign="top"><b>EP-05</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-23</b></td>
      <td valign="top">Consulta de historial de viajes</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero consultar mis viajes anteriores, para revisar el uso que he realizado de biciGO.</td>
      <td valign="top"><b>Escenario 1: Historial disponible</b><br><br><b>Given</b> que el usuario realizó alquileres anteriormente<br><b>When</b> accede a su historial<br><b>Then</b> el sistema muestra sus viajes registrados<br><b>And</b> los organiza para facilitar su consulta.<br><br><b>Escenario 2: Sin viajes previos</b><br><br><b>Given</b> que el usuario todavía no ha utilizado ninguna bicicleta<br><b>When</b> consulta el historial<br><b>Then</b> el sistema informa que aún no existen viajes registrados.<br><br><b>Escenario 3: Selección de viaje</b><br><br><b>Given</b> que existen varios viajes en el historial<br><b>When</b> el usuario selecciona uno<br><b>Then</b> el sistema permite acceder a su información detallada.</td>
      <td valign="top"><b>EP-05</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-24</b></td>
      <td valign="top">Consulta de detalle de viaje</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero consultar el detalle de un viaje realizado, para conocer su duración, distancia y costo final.</td>
      <td valign="top"><b>Escenario 1: Detalle disponible</b><br><br><b>Given</b> que el viaje pertenece al historial del usuario<br><b>When</b> selecciona dicho registro<br><b>Then</b> el sistema muestra la información disponible del viaje<br><b>And</b> presenta el costo correspondiente.<br><br><b>Escenario 2: Registro inexistente</b><br><br><b>Given</b> que el viaje solicitado no existe<br><b>When</b> el usuario intenta consultarlo<br><b>Then</b> el sistema informa que no puede encontrarse.<br><br><b>Escenario 3: Protección de información</b><br><br><b>Given</b> que un viaje pertenece a otro usuario<br><b>When</b> se intenta acceder a su información<br><b>Then</b> el sistema rechaza la solicitud<br><b>And</b> protege los datos asociados.</td>
      <td valign="top"><b>EP-05</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-25</b></td>
      <td valign="top">Cambio de contraseña</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero cambiar mi contraseña desde mi perfil, para mantener segura mi cuenta.</td>
      <td valign="top"><b>Escenario 1: Cambio exitoso</b><br><br><b>Given</b> que el usuario conoce su contraseña actual<br><b>When</b> proporciona la contraseña actual y una nueva contraseña válida<br><b>Then</b> el sistema actualiza sus credenciales<br><b>And</b> confirma que el cambio fue realizado.<br><br><b>Escenario 2: Contraseña actual incorrecta</b><br><br><b>Given</b> que el usuario intenta modificar sus credenciales<br><b>When</b> proporciona una contraseña actual incorrecta<br><b>Then</b> el sistema rechaza el cambio<br><b>And</b> mantiene la contraseña existente.<br><br><b>Escenario 3: Nueva contraseña inválida</b><br><br><b>Given</b> que el usuario está realizando el cambio<br><b>When</b> proporciona una nueva contraseña que no cumple los requisitos<br><b>Then</b> el sistema impide actualizarla<br><b>And</b> informa los requisitos correspondientes.</td>
      <td valign="top"><b>EP-05</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-26</b></td>
      <td valign="top">Reporte de bicicleta dañada</td>
      <td valign="top"><b>Como usuario</b>, quiero reportar una bicicleta que presente daños, para evitar que otros usuarios utilicen una unidad potencialmente insegura.</td>
      <td valign="top"><b>Escenario 1: Reporte exitoso</b><br><br><b>Given</b> que el usuario identifica un problema en una bicicleta<br><b>When</b> registra una descripción válida del daño<br><b>Then</b> el sistema crea el reporte<br><b>And</b> lo asocia con la bicicleta correspondiente.<br><br><b>Escenario 2: Información insuficiente</b><br><br><b>Given</b> que el usuario intenta generar un reporte<br><b>When</b> no proporciona la información requerida<br><b>Then</b> el sistema no registra la incidencia<br><b>And</b> solicita completar los datos necesarios.<br><br><b>Escenario 3: Bicicleta marcada para revisión</b><br><br><b>Given</b> que se registra una incidencia relevante<br><b>When</b> el sistema procesa el reporte<br><b>Then</b> la bicicleta queda marcada para revisión<br><b>And</b> deja de ofrecerse como disponible cuando corresponda.</td>
      <td valign="top"><b>EP-06</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-27</b></td>
      <td valign="top">Reporte de problema durante un viaje</td>
      <td valign="top"><b>Como usuario con un alquiler activo</b>, quiero reportar un problema ocurrido durante mi recorrido, para recibir asistencia y dejar constancia del incidente.</td>
      <td valign="top"><b>Escenario 1: Reporte registrado</b><br><br><b>Given</b> que el usuario posee un viaje activo<br><b>When</b> describe el problema y envía el reporte<br><b>Then</b> el sistema registra la incidencia<br><b>And</b> la relaciona con el alquiler actual.<br><br><b>Escenario 2: Información incompleta</b><br><br><b>Given</b> que el usuario intenta reportar una incidencia<br><b>When</b> no proporciona una descripción suficiente<br><b>Then</b> el sistema solicita completar la información<br><b>And</b> no registra el reporte hasta contar con los datos requeridos.<br><br><b>Escenario 3: Incidencia crítica</b><br><br><b>Given</b> que el problema puede impedir continuar el viaje<br><b>When</b> el usuario lo reporta<br><b>Then</b> el sistema registra la incidencia como prioritaria<br><b>And</b> proporciona las opciones de asistencia disponibles.</td>
      <td valign="top"><b>EP-06</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-28</b></td>
      <td valign="top">Contacto con soporte</td>
      <td valign="top"><b>Como usuario</b>, quiero comunicarme con soporte desde la plataforma, para obtener ayuda ante problemas relacionados con mi cuenta o alquileres.</td>
      <td valign="top"><b>Escenario 1: Solicitud enviada</b><br><br><b>Given</b> que el usuario accede al apartado de soporte<br><b>When</b> describe su consulta y la envía<br><b>Then</b> el sistema registra la solicitud<br><b>And</b> confirma que fue recibida.<br><br><b>Escenario 2: Información incompleta</b><br><br><b>Given</b> que el usuario está creando una solicitud<br><b>When</b> intenta enviarla sin describir el problema<br><b>Then</b> el sistema impide el envío<br><b>And</b> solicita completar la información.<br><br><b>Escenario 3: Solicitud asociada a alquiler</b><br><br><b>Given</b> que el problema corresponde a un viaje específico<br><b>When</b> el usuario selecciona dicho viaje<br><b>Then</b> el sistema relaciona la solicitud con el alquiler correspondiente.</td>
      <td valign="top"><b>EP-06</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-29</b></td>
      <td valign="top">Seguimiento de incidencias</td>
      <td valign="top"><b>Como usuario</b>, quiero consultar el estado de mis incidencias reportadas, para conocer si están pendientes, en revisión o resueltas.</td>
      <td valign="top"><b>Escenario 1: Incidencias disponibles</b><br><br><b>Given</b> que el usuario posee reportes registrados<br><b>When</b> accede a la sección de incidencias<br><b>Then</b> el sistema muestra sus reportes<br><b>And</b> presenta el estado de cada uno.<br><br><b>Escenario 2: Sin incidencias</b><br><br><b>Given</b> que el usuario nunca realizó un reporte<br><b>When</b> consulta esta sección<br><b>Then</b> el sistema informa que no existen incidencias registradas.<br><br><b>Escenario 3: Incidencia actualizada</b><br><br><b>Given</b> que soporte modificó el estado de un reporte<br><b>When</b> el usuario vuelve a consultarlo<br><b>Then</b> el sistema muestra su estado actualizado.</td>
      <td valign="top"><b>EP-06</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-30</b></td>
      <td valign="top">Recepción de notificaciones</td>
      <td valign="top"><b>Como usuario</b>, quiero recibir notificaciones relacionadas con mis alquileres, pagos e incidencias, para mantenerme informado sobre eventos importantes de mi cuenta.</td>
      <td valign="top"><b>Escenario 1: Alquiler iniciado</b><br><br><b>Given</b> que el usuario inicia correctamente un alquiler<br><b>When</b> el sistema confirma la operación<br><b>Then</b> genera una notificación informativa<br><b>And</b> comunica que el viaje fue iniciado.<br><br><b>Escenario 2: Pago procesado</b><br><br><b>Given</b> que se completa el cobro de un alquiler<br><b>When</b> la transacción obtiene un resultado<br><b>Then</b> el sistema informa al usuario si fue aprobada o rechazada.<br><br><b>Escenario 3: Incidencia actualizada</b><br><br><b>Given</b> que existe una incidencia registrada<br><b>When</b> cambia su estado<br><b>Then</b> el sistema notifica al usuario sobre la actualización.</td>
      <td valign="top"><b>EP-06</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-31</b></td>
      <td valign="top">Visualización de flota</td>
      <td valign="top"><b>Como administrador</b>, quiero consultar el estado de las bicicletas de la plataforma, para supervisar la disponibilidad general de la flota.</td>
      <td valign="top"><b>Escenario 1: Consulta exitosa</b><br><br><b>Given</b> que el administrador se encuentra autenticado<br><b>When</b> accede a la gestión de bicicletas<br><b>Then</b> el sistema muestra las unidades registradas<br><b>And</b> presenta su estado actual.<br><br><b>Escenario 2: Bicicleta en uso</b><br><br><b>Given</b> que una bicicleta se encuentra asociada a un alquiler activo<br><b>When</b> el administrador consulta la flota<br><b>Then</b> el sistema la muestra como ocupada.<br><br><b>Escenario 3: Bicicleta fuera de servicio</b><br><br><b>Given</b> que una bicicleta requiere mantenimiento<br><b>When</b> el administrador revisa la flota<br><b>Then</b> el sistema la muestra como fuera de servicio.</td>
      <td valign="top"><b>EP-07</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-32</b></td>
      <td valign="top">Actualización del estado de bicicleta</td>
      <td valign="top"><b>Como administrador</b>, quiero modificar el estado operativo de una bicicleta, para controlar qué unidades pueden ser alquiladas por los usuarios.</td>
      <td valign="top"><b>Escenario 1: Cambio a mantenimiento</b><br><br><b>Given</b> que una bicicleta presenta un problema<br><b>When</b> el administrador la marca como en mantenimiento<br><b>Then</b> el sistema actualiza su estado<br><b>And</b> evita nuevos alquileres.<br><br><b>Escenario 2: Retorno al servicio</b><br><br><b>Given</b> que una bicicleta fue reparada<br><b>When</b> el administrador la marca nuevamente como disponible<br><b>Then</b> el sistema actualiza su estado<br><b>And</b> permite que vuelva a mostrarse a los usuarios.<br><br><b>Escenario 3: Bicicleta con alquiler activo</b><br><br><b>Given</b> que una bicicleta está actualmente alquilada<br><b>When</b> se intenta modificar su estado de forma incompatible<br><b>Then</b> el sistema rechaza la operación<br><b>And</b> informa que existe un alquiler activo.</td>
      <td valign="top"><b>EP-07</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-33</b></td>
      <td valign="top">Gestión de incidencias de bicicletas</td>
      <td valign="top"><b>Como administrador</b>, quiero revisar los reportes relacionados con bicicletas dañadas, para priorizar su mantenimiento y mantener segura la flota.</td>
      <td valign="top"><b>Escenario 1: Reportes disponibles</b><br><br><b>Given</b> que existen incidencias registradas por los usuarios<br><b>When</b> el administrador accede a la gestión de incidencias<br><b>Then</b> el sistema muestra los reportes pendientes.<br><br><b>Escenario 2: Cambio de estado</b><br><br><b>Given</b> que una incidencia está pendiente<br><b>When</b> el administrador inicia su revisión<br><b>Then</b> el sistema permite actualizar su estado<br><b>And</b> registra el cambio realizado.<br><br><b>Escenario 3: Incidencia resuelta</b><br><br><b>Given</b> que el problema de una bicicleta fue solucionado<br><b>When</b> el administrador marca la incidencia como resuelta<br><b>Then</b> el sistema registra su resolución<br><b>And</b> conserva el reporte en el historial.</td>
      <td valign="top"><b>EP-07</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-34</b></td>
      <td valign="top">Consulta de métricas de alquiler</td>
      <td valign="top"><b>Como administrador</b>, quiero visualizar métricas de uso de las bicicletas, para analizar el comportamiento del servicio y apoyar decisiones operativas.</td>
      <td valign="top"><b>Escenario 1: Datos disponibles</b><br><br><b>Given</b> que existen alquileres registrados<br><b>When</b> el administrador accede al dashboard<br><b>Then</b> el sistema muestra las métricas disponibles<br><b>And</b> presenta información sobre el uso de la plataforma.<br><br><b>Escenario 2: Periodo seleccionado</b><br><br><b>Given</b> que existen datos correspondientes a distintos periodos<br><b>When</b> el administrador selecciona un rango de fechas<br><b>Then</b> el sistema actualiza las métricas<br><b>And</b> utiliza únicamente los datos del periodo indicado.<br><br><b>Escenario 3: Sin información</b><br><br><b>Given</b> que no existen alquileres para el periodo seleccionado<br><b>When</b> se realiza la consulta<br><b>Then</b> el sistema informa que no existen datos suficientes para mostrar resultados.</td>
      <td valign="top"><b>EP-07</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-35</b></td>
      <td valign="top">Gestión de usuarios</td>
      <td valign="top"><b>Como administrador</b>, quiero consultar y gestionar las cuentas de los usuarios, para atender situaciones que puedan afectar la seguridad o el correcto funcionamiento de biciGO.</td>
      <td valign="top"><b>Escenario 1: Consulta de usuarios</b><br><br><b>Given</b> que el administrador posee los permisos correspondientes<br><b>When</b> accede al listado de usuarios<br><b>Then</b> el sistema muestra las cuentas registradas<br><b>And</b> permite consultar su estado.<br><br><b>Escenario 2: Restricción de cuenta</b><br><br><b>Given</b> que existe una razón válida para restringir una cuenta<br><b>When</b> el administrador aplica la restricción<br><b>Then</b> el sistema actualiza su estado<br><b>And</b> impide iniciar nuevos alquileres según corresponda.<br><br><b>Escenario 3: Reactivación de cuenta</b><br><br><b>Given</b> que una cuenta se encuentra restringida<br><b>When</b> el administrador determina que puede reactivarse<br><b>Then</b> el sistema elimina la restricción<br><b>And</b> restablece las funcionalidades correspondientes.</td>
      <td valign="top"><b>EP-07</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-36</b></td>
      <td valign="top">Eliminación de método de pago</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero eliminar un método de pago que ya no utilizo, para mantener actualizadas mis opciones de cobro.</td>
      <td valign="top"><b>Escenario 1: Eliminación exitosa</b><br><br><b>Given</b> que el usuario posee un método de pago registrado que no está asociado a una operación pendiente<br><b>When</b> selecciona dicho método y confirma su eliminación<br><b>Then</b> el sistema elimina el método seleccionado<br><b>And</b> actualiza la lista de métodos disponibles.<br><br><b>Escenario 2: Método asociado a un pago pendiente</b><br><br><b>Given</b> que el método seleccionado está vinculado a una transacción pendiente<br><b>When</b> el usuario intenta eliminarlo<br><b>Then</b> el sistema rechaza temporalmente la eliminación<br><b>And</b> informa que primero debe resolverse la transacción pendiente.<br><br><b>Escenario 3: Método inexistente</b><br><br><b>Given</b> que el método de pago ya fue eliminado o no pertenece al usuario<br><b>When</b> se intenta procesar nuevamente su eliminación<br><b>Then</b> el sistema no realiza cambios<br><b>And</b> informa que el método no está disponible.</td>
      <td valign="top"><b>EP-04</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-37</b></td>
      <td valign="top">Consulta de comprobantes de pago</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero consultar los comprobantes de mis pagos realizados, para revisar los cargos asociados a mis alquileres y suscripciones.</td>
      <td valign="top"><b>Escenario 1: Comprobantes disponibles</b><br><br><b>Given</b> que el usuario posee pagos completados<br><b>When</b> accede a la sección de comprobantes<br><b>Then</b> el sistema muestra los comprobantes registrados<br><b>And</b> permite consultar su información principal.<br><br><b>Escenario 2: Sin comprobantes</b><br><br><b>Given</b> que el usuario aún no ha realizado pagos<br><b>When</b> accede a la sección de comprobantes<br><b>Then</b> el sistema informa que no existen comprobantes disponibles.<br><br><b>Escenario 3: Consulta de un comprobante</b><br><br><b>Given</b> que existe un comprobante asociado al usuario<br><b>When</b> selecciona dicho registro<br><b>Then</b> el sistema muestra el detalle del pago correspondiente<br><b>And</b> relaciona el comprobante con el servicio pagado.</td>
      <td valign="top"><b>EP-04</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-38</b></td>
      <td valign="top">Configuración de notificaciones</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero configurar qué notificaciones deseo recibir, para controlar los avisos enviados por biciGO.</td>
      <td valign="top"><b>Escenario 1: Actualización exitosa</b><br><br><b>Given</b> que el usuario accede a la configuración de notificaciones<br><b>When</b> activa o desactiva una categoría disponible<br><b>Then</b> el sistema guarda la nueva preferencia<br><b>And</b> la aplica a futuras notificaciones opcionales.<br><br><b>Escenario 2: Configuración sin cambios</b><br><br><b>Given</b> que el usuario mantiene las preferencias actuales<br><b>When</b> sale de la configuración sin modificar opciones<br><b>Then</b> el sistema conserva la configuración existente.<br><br><b>Escenario 3: Aviso operativo obligatorio</b><br><br><b>Given</b> que ocurre un evento crítico que requiere informar al usuario<br><b>When</b> la plataforma genera la notificación correspondiente<br><b>Then</b> el sistema envía el aviso operativo<br><b>And</b> mantiene informada a la persona sobre la operación crítica.</td>
      <td valign="top"><b>EP-06</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-39</b></td>
      <td valign="top">Consulta de zonas de cobertura</td>
      <td valign="top"><b>Como usuario</b>, quiero consultar las zonas donde opera biciGO, para saber si el servicio está disponible en el lugar donde deseo utilizar una bicicleta.</td>
      <td valign="top"><b>Escenario 1: Zona con cobertura</b><br><br><b>Given</b> que el usuario consulta una ubicación incluida en el área de operación<br><b>When</b> selecciona o busca dicha zona<br><b>Then</b> el sistema indica que existe cobertura<br><b>And</b> permite visualizar las bicicletas disponibles en el área.<br><br><b>Escenario 2: Zona sin cobertura</b><br><br><b>Given</b> que el usuario consulta una ubicación fuera del área de operación<br><b>When</b> realiza la búsqueda<br><b>Then</b> el sistema informa que biciGO aún no opera en esa zona.<br><br><b>Escenario 3: Cobertura actualizada</b><br><br><b>Given</b> que se incorpora una nueva zona de operación<br><b>When</b> el usuario vuelve a consultar el mapa de cobertura<br><b>Then</b> el sistema muestra la nueva zona disponible.</td>
      <td valign="top"><b>EP-02</b></td>
    </tr>
    <tr>
      <td valign="top"><b>US-40</b></td>
      <td valign="top">Desactivación de cuenta</td>
      <td valign="top"><b>Como usuario registrado</b>, quiero desactivar mi cuenta cuando ya no desee utilizar biciGO, para dejar de acceder a los servicios de la plataforma.</td>
      <td valign="top"><b>Escenario 1: Desactivación exitosa</b><br><br><b>Given</b> que el usuario no posee alquileres ni pagos pendientes<br><b>When</b> solicita desactivar su cuenta y confirma la acción<br><b>Then</b> el sistema cambia la cuenta a estado inactivo<br><b>And</b> finaliza las sesiones activas.<br><br><b>Escenario 2: Alquiler activo</b><br><br><b>Given</b> que el usuario mantiene un alquiler en curso<br><b>When</b> intenta desactivar su cuenta<br><b>Then</b> el sistema rechaza temporalmente la solicitud<br><b>And</b> indica que primero debe finalizar el alquiler.<br><br><b>Escenario 3: Pago pendiente</b><br><br><b>Given</b> que el usuario posee una transacción pendiente<br><b>When</b> solicita desactivar su cuenta<br><b>Then</b> el sistema impide completar la desactivación<br><b>And</b> informa que primero debe resolver el pago pendiente.</td>
      <td valign="top"><b>EP-05</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-01</b></td>
      <td valign="top">Register Passenger</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar el endpoint de registro de usuario, para permitir la creación de cuentas en la plataforma.</td>
      <td valign="top"><b>Escenario 1: Registro exitoso</b><br><br><b>Given</b> que un cliente envía una petición con correo válido, contraseña y datos obligatorios<br><b>When</b> el endpoint <code>POST /api/auth/register</code> procesa la solicitud<br><b>Then</b> el sistema crea el usuario con estado activo<br><b>And</b> retorna <code>201 Created</code> con el identificador y correo del usuario.<br><br><b>Escenario 2: Correo duplicado</b><br><br><b>Given</b> que un cliente envía una petición con un correo ya registrado<br><b>When</b> el endpoint <code>POST /api/auth/register</code> procesa la solicitud<br><b>Then</b> el sistema retorna <code>409 Conflict</code><br><b>And</b> no crea un nuevo registro.<br><br><b>Escenario 3: Datos inválidos</b><br><br><b>Given</b> que la solicitud contiene campos obligatorios vacíos o con formato inválido<br><b>When</b> el endpoint valida el cuerpo de la petición<br><b>Then</b> el sistema retorna <code>400 Bad Request</code><br><b>And</b> informa los campos que deben corregirse.</td>
      <td valign="top"><b>EP-01</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-02</b></td>
      <td valign="top">Login User</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar el endpoint de inicio de sesión, para autenticar usuarios y permitir el acceso seguro a las funciones privadas.</td>
      <td valign="top"><b>Escenario 1: Autenticación exitosa</b><br><br><b>Given</b> que el cliente envía un correo registrado y una contraseña válida<br><b>When</b> el endpoint <code>POST /api/auth/login</code> procesa las credenciales<br><b>Then</b> el sistema autentica al usuario y genera un token de acceso<br><b>And</b> retorna <code>200 OK</code> con la información necesaria para la sesión.<br><br><b>Escenario 2: Credenciales incorrectas</b><br><br><b>Given</b> que el correo existe pero la contraseña no coincide<br><b>When</b> el endpoint procesa la solicitud<br><b>Then</b> el sistema rechaza la autenticación<br><b>And</b> retorna <code>401 Unauthorized</code>.<br><br><b>Escenario 3: Usuario inexistente</b><br><br><b>Given</b> que el cliente envía un correo no registrado<br><b>When</b> el endpoint intenta autenticar la cuenta<br><b>Then</b> el sistema rechaza el acceso<br><b>And</b> retorna <code>401 Unauthorized</code> sin exponer información sensible.</td>
      <td valign="top"><b>EP-01</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-03</b></td>
      <td valign="top">Recover Password</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar el proceso de recuperación de contraseña, para que un usuario pueda restablecer sus credenciales de forma segura.</td>
      <td valign="top"><b>Escenario 1: Solicitud válida</b><br><br><b>Given</b> que el cliente envía un correo asociado a una cuenta<br><b>When</b> el endpoint <code>POST /api/auth/password/recovery</code> procesa la solicitud<br><b>Then</b> el sistema genera un token temporal de recuperación<br><b>And</b> retorna <code>200 OK</code> e inicia el flujo de restablecimiento.<br><br><b>Escenario 2: Token inválido</b><br><br><b>Given</b> que el usuario intenta cambiar la contraseña con un token inexistente o alterado<br><b>When</b> el endpoint de restablecimiento valida el token<br><b>Then</b> el sistema rechaza la operación<br><b>And</b> retorna <code>400 Bad Request</code>.<br><br><b>Escenario 3: Token expirado</b><br><br><b>Given</b> que el token superó su tiempo de vigencia<br><b>When</b> el usuario intenta utilizarlo<br><b>Then</b> el sistema impide modificar la contraseña<br><b>And</b> retorna <code>410 Gone</code> o una respuesta equivalente definida por la API.</td>
      <td valign="top"><b>EP-01</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-04</b></td>
      <td valign="top">Verify Account</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar la verificación de cuenta, para habilitar únicamente usuarios que hayan completado correctamente el proceso de validación.</td>
      <td valign="top"><b>Escenario 1: Verificación exitosa</b><br><br><b>Given</b> que existe una cuenta pendiente y el cliente posee un código válido<br><b>When</b> el endpoint <code>POST /api/auth/verify</code> procesa la solicitud<br><b>Then</b> el sistema actualiza la cuenta como verificada<br><b>And</b> retorna <code>200 OK</code>.<br><br><b>Escenario 2: Código inválido</b><br><br><b>Given</b> que el código proporcionado no corresponde a la cuenta<br><b>When</b> el endpoint valida la solicitud<br><b>Then</b> el sistema no modifica el estado del usuario<br><b>And</b> retorna <code>400 Bad Request</code>.<br><br><b>Escenario 3: Cuenta ya verificada</b><br><br><b>Given</b> que la cuenta ya se encuentra verificada<br><b>When</b> el cliente intenta repetir el proceso<br><b>Then</b> el sistema conserva el estado actual<br><b>And</b> retorna una respuesta informativa sin duplicar la operación.</td>
      <td valign="top"><b>EP-01</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-05</b></td>
      <td valign="top">Get Nearby Bikes</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar la consulta de bicicletas cercanas, para mostrar al usuario las unidades disponibles según su ubicación.</td>
      <td valign="top"><b>Escenario 1: Bicicletas encontradas</b><br><br><b>Given</b> que el cliente envía coordenadas válidas dentro de una zona con cobertura<br><b>When</b> el endpoint <code>GET /api/bikes/nearby?lat={lat}&lng={lng}</code> procesa la consulta<br><b>Then</b> el sistema obtiene las bicicletas disponibles cercanas<br><b>And</b> retorna <code>200 OK</code> con la lista de unidades.<br><br><b>Escenario 2: Sin bicicletas disponibles</b><br><br><b>Given</b> que la ubicación es válida pero no existen unidades disponibles<br><b>When</b> el endpoint procesa la consulta<br><b>Then</b> el sistema devuelve una lista vacía<br><b>And</b> retorna <code>200 OK</code>.<br><br><b>Escenario 3: Coordenadas inválidas</b><br><br><b>Given</b> que la latitud o longitud poseen un formato o rango incorrecto<br><b>When</b> el endpoint valida los parámetros<br><b>Then</b> el sistema rechaza la consulta<br><b>And</b> retorna <code>400 Bad Request</code>.</td>
      <td valign="top"><b>EP-02</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-06</b></td>
      <td valign="top">Get Bike Detail</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar el detalle de una bicicleta, para exponer su estado y datos necesarios antes de iniciar un alquiler.</td>
      <td valign="top"><b>Escenario 1: Bicicleta encontrada</b><br><br><b>Given</b> que existe una bicicleta con el identificador solicitado<br><b>When</b> el endpoint <code>GET /api/bikes/{bikeId}</code> procesa la consulta<br><b>Then</b> el sistema recupera la información de la bicicleta<br><b>And</b> retorna <code>200 OK</code> con su estado actual.<br><br><b>Escenario 2: Bicicleta inexistente</b><br><br><b>Given</b> que no existe una bicicleta con el identificador recibido<br><b>When</b> el endpoint procesa la solicitud<br><b>Then</b> el sistema no encuentra el recurso<br><b>And</b> retorna <code>404 Not Found</code>.<br><br><b>Escenario 3: Bicicleta en mantenimiento</b><br><br><b>Given</b> que la bicicleta existe pero está fuera de servicio<br><b>When</b> el usuario consulta su detalle<br><b>Then</b> el sistema retorna la información con estado de mantenimiento<br><b>And</b> impide que sea tratada como disponible.</td>
      <td valign="top"><b>EP-02</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-07</b></td>
      <td valign="top">Search Coverage Zone</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar la consulta de zonas de cobertura, para indicar si biciGO opera en una ubicación determinada.</td>
      <td valign="top"><b>Escenario 1: Zona con cobertura</b><br><br><b>Given</b> que el cliente envía una ubicación válida dentro del área de operación<br><b>When</b> el endpoint <code>GET /api/coverage</code> procesa la consulta<br><b>Then</b> el sistema identifica la zona como cubierta<br><b>And</b> retorna <code>200 OK</code> con la información de cobertura.<br><br><b>Escenario 2: Zona sin cobertura</b><br><br><b>Given</b> que la ubicación consultada está fuera del área de operación<br><b>When</b> el endpoint procesa la solicitud<br><b>Then</b> el sistema indica que no existe cobertura<br><b>And</b> retorna <code>200 OK</code> con el estado correspondiente.<br><br><b>Escenario 3: Parámetros inválidos</b><br><br><b>Given</b> que la consulta no contiene la información mínima requerida<br><b>When</b> el endpoint valida los parámetros<br><b>Then</b> el sistema rechaza la solicitud<br><b>And</b> retorna <code>400 Bad Request</code>.</td>
      <td valign="top"><b>EP-02</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-08</b></td>
      <td valign="top">Start Rental</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar el endpoint para iniciar un alquiler, para asociar una bicicleta disponible con un usuario autenticado.</td>
      <td valign="top"><b>Escenario 1: Alquiler iniciado</b><br><br><b>Given</b> que el usuario está autenticado, no posee otro alquiler activo y la bicicleta está disponible<br><b>When</b> el endpoint <code>POST /api/rentals</code> procesa la solicitud<br><b>Then</b> el sistema crea el alquiler y cambia la bicicleta a estado ocupado<br><b>And</b> retorna <code>201 Created</code> con el identificador del alquiler.<br><br><b>Escenario 2: Bicicleta no disponible</b><br><br><b>Given</b> que la bicicleta ya está alquilada o fuera de servicio<br><b>When</b> el cliente intenta iniciar el alquiler<br><b>Then</b> el sistema rechaza la operación<br><b>And</b> retorna <code>409 Conflict</code>.<br><br><b>Escenario 3: Usuario con alquiler activo</b><br><br><b>Given</b> que el usuario ya posee un alquiler en curso<br><b>When</b> el endpoint procesa una nueva solicitud<br><b>Then</b> el sistema impide crear otro alquiler<br><b>And</b> retorna <code>409 Conflict</code>.</td>
      <td valign="top"><b>EP-03</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-09</b></td>
      <td valign="top">Unlock Bike</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar la validación del código de desbloqueo, para autorizar únicamente la apertura de la bicicleta asociada al alquiler vigente.</td>
      <td valign="top"><b>Escenario 1: Código válido</b><br><br><b>Given</b> que existe un alquiler activo y el código corresponde a la bicicleta asignada<br><b>When</b> el endpoint <code>POST /api/rentals/{rentalId}/unlock</code> procesa la solicitud<br><b>Then</b> el sistema valida el código y autoriza el desbloqueo<br><b>And</b> retorna <code>200 OK</code>.<br><br><b>Escenario 2: Código incorrecto</b><br><br><b>Given</b> que el código enviado no coincide con el alquiler<br><b>When</b> el endpoint valida la solicitud<br><b>Then</b> el sistema rechaza el desbloqueo<br><b>And</b> retorna <code>400 Bad Request</code>.<br><br><b>Escenario 3: Alquiler inexistente</b><br><br><b>Given</b> que el identificador de alquiler no existe o no pertenece al usuario<br><b>When</b> el cliente solicita el desbloqueo<br><b>Then</b> el sistema rechaza la operación<br><b>And</b> retorna <code>404 Not Found</code> o <code>403 Forbidden</code> según corresponda.</td>
      <td valign="top"><b>EP-03</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-10</b></td>
      <td valign="top">Get Active Rental</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar la consulta del alquiler activo, para mostrar al usuario la información actual de su viaje.</td>
      <td valign="top"><b>Escenario 1: Viaje activo</b><br><br><b>Given</b> que el usuario posee un alquiler en curso<br><b>When</b> el endpoint <code>GET /api/rentals/active</code> procesa la consulta<br><b>Then</b> el sistema recupera los datos del alquiler vigente<br><b>And</b> retorna <code>200 OK</code> con su información.<br><br><b>Escenario 2: Sin viaje activo</b><br><br><b>Given</b> que el usuario no posee ningún alquiler vigente<br><b>When</b> el endpoint procesa la consulta<br><b>Then</b> el sistema no encuentra un alquiler activo<br><b>And</b> retorna <code>204 No Content</code> o la respuesta definida por la API.<br><br><b>Escenario 3: Usuario no autenticado</b><br><br><b>Given</b> que la solicitud no contiene credenciales válidas<br><b>When</b> el cliente intenta consultar el alquiler<br><b>Then</b> el sistema bloquea el acceso<br><b>And</b> retorna <code>401 Unauthorized</code>.</td>
      <td valign="top"><b>EP-03</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-11</b></td>
      <td valign="top">Finish Rental</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar el endpoint de finalización de alquiler, para cerrar el viaje, calcular el importe y liberar la bicicleta.</td>
      <td valign="top"><b>Escenario 1: Finalización exitosa</b><br><br><b>Given</b> que existe un alquiler activo válido<br><b>When</b> el endpoint <code>POST /api/rentals/{rentalId}/finish</code> procesa la solicitud<br><b>Then</b> el sistema registra la hora final, calcula el costo y libera la bicicleta<br><b>And</b> retorna <code>200 OK</code> con el resumen del viaje.<br><br><b>Escenario 2: Alquiler ya finalizado</b><br><br><b>Given</b> que el alquiler solicitado ya se encuentra cerrado<br><b>When</b> el cliente intenta finalizarlo nuevamente<br><b>Then</b> el sistema evita duplicar el cierre<br><b>And</b> retorna <code>409 Conflict</code>.<br><br><b>Escenario 3: Alquiler inexistente</b><br><br><b>Given</b> que no existe un alquiler con el identificador recibido<br><b>When</b> el endpoint procesa la solicitud<br><b>Then</b> el sistema no encuentra el recurso<br><b>And</b> retorna <code>404 Not Found</code>.</td>
      <td valign="top"><b>EP-03</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-12</b></td>
      <td valign="top">Register Payment Method</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar el registro de métodos de pago, para permitir que los usuarios dispongan de una opción válida para realizar cobros.</td>
      <td valign="top"><b>Escenario 1: Método registrado</b><br><br><b>Given</b> que el usuario autenticado envía datos válidos de un método de pago<br><b>When</b> el endpoint <code>POST /api/payments/methods</code> procesa la solicitud<br><b>Then</b> el sistema registra la referencia segura del método<br><b>And</b> retorna <code>201 Created</code>.<br><br><b>Escenario 2: Datos inválidos</b><br><br><b>Given</b> que la información enviada no cumple las reglas del proveedor de pagos<br><b>When</b> el endpoint intenta validar el método<br><b>Then</b> el sistema rechaza el registro<br><b>And</b> retorna <code>400 Bad Request</code>.<br><br><b>Escenario 3: Error del proveedor</b><br><br><b>Given</b> que el servicio externo de pagos no puede validar el método<br><b>When</b> el backend procesa la respuesta del proveedor<br><b>Then</b> el sistema no registra el método como válido<br><b>And</b> retorna una respuesta de error controlada.</td>
      <td valign="top"><b>EP-04</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-13</b></td>
      <td valign="top">Process Rental Payment</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar el procesamiento del pago de un alquiler, para registrar el cobro correspondiente al servicio utilizado.</td>
      <td valign="top"><b>Escenario 1: Pago aprobado</b><br><br><b>Given</b> que existe un alquiler finalizado con importe pendiente y un método de pago válido<br><b>When</b> el endpoint <code>POST /api/payments/rentals/{rentalId}</code> procesa el cobro<br><b>Then</b> el sistema registra la transacción como aprobada<br><b>And</b> retorna <code>200 OK</code> con el identificador de pago.<br><br><b>Escenario 2: Pago rechazado</b><br><br><b>Given</b> que el proveedor rechaza la transacción<br><b>When</b> el backend recibe la respuesta<br><b>Then</b> el sistema mantiene el pago como pendiente o rechazado<br><b>And</b> retorna una respuesta que informa el resultado sin marcar la deuda como pagada.<br><br><b>Escenario 3: Reintento duplicado</b><br><br><b>Given</b> que una solicitud de pago ya fue procesada con la misma clave de idempotencia<br><b>When</b> el cliente reenvía la operación<br><b>Then</b> el sistema no realiza un segundo cobro<br><b>And</b> retorna el resultado previamente registrado.</td>
      <td valign="top"><b>EP-04</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-14</b></td>
      <td valign="top">Manage Subscription</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar la gestión de suscripciones, para permitir activar y cancelar planes mensuales de biciGO.</td>
      <td valign="top"><b>Escenario 1: Suscripción activada</b><br><br><b>Given</b> que el usuario no posee el mismo plan activo y el pago es aprobado<br><b>When</b> el endpoint <code>POST /api/subscriptions</code> procesa la solicitud<br><b>Then</b> el sistema crea la suscripción con su periodo de vigencia<br><b>And</b> retorna <code>201 Created</code>.<br><br><b>Escenario 2: Suscripción duplicada</b><br><br><b>Given</b> que el usuario ya posee el mismo plan activo<br><b>When</b> intenta contratarlo nuevamente<br><b>Then</b> el sistema rechaza la operación<br><b>And</b> retorna <code>409 Conflict</code>.<br><br><b>Escenario 3: Cancelación exitosa</b><br><br><b>Given</b> que existe una suscripción vigente<br><b>When</b> el endpoint <code>DELETE /api/subscriptions/{subscriptionId}</code> procesa la solicitud<br><b>Then</b> el sistema desactiva la renovación automática<br><b>And</b> retorna <code>200 OK</code> conservando la vigencia ya pagada.</td>
      <td valign="top"><b>EP-04</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-15</b></td>
      <td valign="top">Get User Profile</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar la consulta y actualización del perfil, para permitir que cada usuario gestione sus datos personales.</td>
      <td valign="top"><b>Escenario 1: Perfil obtenido</b><br><br><b>Given</b> que el usuario se encuentra autenticado<br><b>When</b> el endpoint <code>GET /api/users/me</code> procesa la consulta<br><b>Then</b> el sistema recupera únicamente la información del usuario autenticado<br><b>And</b> retorna <code>200 OK</code>.<br><br><b>Escenario 2: Perfil actualizado</b><br><br><b>Given</b> que el usuario envía datos válidos<br><b>When</b> el endpoint <code>PUT /api/users/me</code> procesa la solicitud<br><b>Then</b> el sistema actualiza la información permitida<br><b>And</b> retorna <code>200 OK</code> con los datos actualizados.<br><br><b>Escenario 3: Datos inválidos</b><br><br><b>Given</b> que la solicitud contiene información con formato incorrecto<br><b>When</b> el endpoint valida los campos<br><b>Then</b> el sistema rechaza la actualización<br><b>And</b> retorna <code>400 Bad Request</code>.</td>
      <td valign="top"><b>EP-05</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-16</b></td>
      <td valign="top">Get Travel History</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar la consulta del historial de viajes, para mostrar únicamente los alquileres pertenecientes al usuario autenticado.</td>
      <td valign="top"><b>Escenario 1: Historial disponible</b><br><br><b>Given</b> que el usuario posee alquileres finalizados<br><b>When</b> el endpoint <code>GET /api/rentals/history</code> procesa la consulta<br><b>Then</b> el sistema recupera sus viajes registrados<br><b>And</b> retorna <code>200 OK</code> con la lista correspondiente.<br><br><b>Escenario 2: Historial vacío</b><br><br><b>Given</b> que el usuario aún no ha realizado viajes<br><b>When</b> el endpoint procesa la consulta<br><b>Then</b> el sistema devuelve una colección vacía<br><b>And</b> retorna <code>200 OK</code>.<br><br><b>Escenario 3: Acceso a viaje ajeno</b><br><br><b>Given</b> que el usuario intenta consultar un alquiler que pertenece a otra cuenta<br><b>When</b> el endpoint valida la propiedad del recurso<br><b>Then</b> el sistema rechaza el acceso<br><b>And</b> retorna <code>403 Forbidden</code>.</td>
      <td valign="top"><b>EP-05</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-17</b></td>
      <td valign="top">Create Incident</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar el registro de incidencias, para almacenar reportes relacionados con bicicletas y viajes.</td>
      <td valign="top"><b>Escenario 1: Incidencia creada</b><br><br><b>Given</b> que el usuario envía una descripción válida y una referencia de bicicleta o alquiler<br><b>When</b> el endpoint <code>POST /api/incidents</code> procesa la solicitud<br><b>Then</b> el sistema crea el reporte con estado pendiente<br><b>And</b> retorna <code>201 Created</code> con su identificador.<br><br><b>Escenario 2: Datos incompletos</b><br><br><b>Given</b> que la solicitud no incluye la información obligatoria<br><b>When</b> el endpoint valida el cuerpo<br><b>Then</b> el sistema rechaza la creación<br><b>And</b> retorna <code>400 Bad Request</code>.<br><br><b>Escenario 3: Recurso relacionado inexistente</b><br><br><b>Given</b> que la bicicleta o alquiler indicado no existe<br><b>When</b> el endpoint procesa la solicitud<br><b>Then</b> el sistema no crea la incidencia<br><b>And</b> retorna <code>404 Not Found</code>.</td>
      <td valign="top"><b>EP-06</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-18</b></td>
      <td valign="top">Get Incident Status</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar la consulta del estado de incidencias, para que el usuario pueda dar seguimiento a sus reportes.</td>
      <td valign="top"><b>Escenario 1: Incidencias encontradas</b><br><br><b>Given</b> que el usuario posee reportes registrados<br><b>When</b> el endpoint <code>GET /api/incidents</code> procesa la consulta<br><b>Then</b> el sistema devuelve únicamente las incidencias pertenecientes al usuario<br><b>And</b> retorna <code>200 OK</code>.<br><br><b>Escenario 2: Incidencia específica</b><br><br><b>Given</b> que existe una incidencia perteneciente al usuario<br><b>When</b> el endpoint <code>GET /api/incidents/{incidentId}</code> procesa la solicitud<br><b>Then</b> el sistema devuelve el detalle y estado actual<br><b>And</b> retorna <code>200 OK</code>.<br><br><b>Escenario 3: Incidencia ajena</b><br><br><b>Given</b> que el identificador pertenece a otro usuario<br><b>When</b> el cliente intenta consultarlo<br><b>Then</b> el sistema rechaza el acceso<br><b>And</b> retorna <code>403 Forbidden</code>.</td>
      <td valign="top"><b>EP-06</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-19</b></td>
      <td valign="top">Manage Bike Status</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar endpoints administrativos para actualizar el estado de las bicicletas, para controlar disponibilidad y mantenimiento de la flota.</td>
      <td valign="top"><b>Escenario 1: Cambio a mantenimiento</b><br><br><b>Given</b> que un administrador autenticado selecciona una bicicleta disponible<br><b>When</b> el endpoint <code>PATCH /api/admin/bikes/{bikeId}/status</code> recibe el estado <code>MAINTENANCE</code><br><b>Then</b> el sistema actualiza la bicicleta<br><b>And</b> retorna <code>200 OK</code>.<br><br><b>Escenario 2: Retorno a disponible</b><br><br><b>Given</b> que una bicicleta en mantenimiento ya fue reparada<br><b>When</b> el administrador cambia su estado a <code>AVAILABLE</code><br><b>Then</b> el sistema actualiza la unidad<br><b>And</b> retorna <code>200 OK</code>.<br><br><b>Escenario 3: Usuario sin permisos</b><br><br><b>Given</b> que un usuario sin rol administrativo intenta modificar el estado<br><b>When</b> el endpoint valida su autorización<br><b>Then</b> el sistema rechaza la operación<br><b>And</b> retorna <code>403 Forbidden</code>.</td>
      <td valign="top"><b>EP-07</b></td>
    </tr>
    <tr>
      <td valign="top"><b>TS-20</b></td>
      <td valign="top">Get Dashboard Metrics</td>
      <td valign="top"><b>Como desarrollador</b>, quiero implementar las consultas del dashboard administrativo, para obtener métricas de alquileres, usuarios y disponibilidad de bicicletas.</td>
      <td valign="top"><b>Escenario 1: Métricas disponibles</b><br><br><b>Given</b> que existen datos registrados en el periodo solicitado<br><b>When</b> el endpoint <code>GET /api/admin/metrics?from={date}&to={date}</code> procesa la consulta<br><b>Then</b> el sistema calcula y devuelve las métricas correspondientes<br><b>And</b> retorna <code>200 OK</code>.<br><br><b>Escenario 2: Periodo sin datos</b><br><br><b>Given</b> que no existen registros en el rango indicado<br><b>When</b> el endpoint procesa la consulta<br><b>Then</b> el sistema devuelve métricas vacías o con valor cero según corresponda<br><b>And</b> retorna <code>200 OK</code>.<br><br><b>Escenario 3: Rango inválido</b><br><br><b>Given</b> que la fecha inicial es posterior a la fecha final<br><b>When</b> el endpoint valida los parámetros<br><b>Then</b> el sistema rechaza la consulta<br><b>And</b> retorna <code>400 Bad Request</code>.</td>
      <td valign="top"><b>EP-07</b></td>
    </tr>
</table>

## 3.2. Impact Mapping

<p align="center">
  <img src="./Resources/Capitulo3/ImpactMap.png" width="100%">
</p>

## 3.3. Product Backlog

<table border="1" cellspacing="0" cellpadding="7" style="border-collapse: collapse; width: 100%; border: 2px solid black;">
  <tr>
    <th align="center"># Orden</th>
    <th align="center">User Story Id</th>
    <th align="center">Título</th>
    <th align="center">Descripción</th>
    <th align="center">Story Points<br>(1 / 2 / 3 / 5 / 8)</th>
  </tr>
  <tr>
    <td valign="top" align="center"><b>1</b></td>
    <td valign="top" align="center"><b>US-39</b></td>
    <td valign="top">Consulta de zonas de cobertura</td>
    <td valign="top">Como usuario , quiero consultar las zonas donde opera biciGO, para saber si el servicio está disponible en el lugar donde deseo utilizar una bicicleta.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>2</b></td>
    <td valign="top" align="center"><b>US-07</b></td>
    <td valign="top">Visualización de bicicletas cercanas</td>
    <td valign="top">Como usuario registrado , quiero visualizar las bicicletas disponibles cerca de mi ubicación, para elegir una alternativa conveniente para mi viaje.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>3</b></td>
    <td valign="top" align="center"><b>US-08</b></td>
    <td valign="top">Consulta de información de bicicleta</td>
    <td valign="top">Como usuario registrado , quiero consultar la información de una bicicleta, para verificar su disponibilidad y condición antes de alquilarla.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>4</b></td>
    <td valign="top" align="center"><b>US-17</b></td>
    <td valign="top">Consulta de tarifa</td>
    <td valign="top">Como usuario registrado , quiero consultar la tarifa aplicable al alquiler, para conocer las condiciones de cobro antes de utilizar una bicicleta.</td>
    <td valign="top" align="center"><b>2</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>5</b></td>
    <td valign="top" align="center"><b>US-01</b></td>
    <td valign="top">Registro de usuario</td>
    <td valign="top">Como visitante , quiero registrarme en biciGO proporcionando mis datos personales y credenciales, para poder acceder a los servicios de alquiler de bicicletas.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>6</b></td>
    <td valign="top" align="center"><b>US-02</b></td>
    <td valign="top">Inicio de sesión</td>
    <td valign="top">Como usuario registrado , quiero iniciar sesión con mis credenciales, para acceder de forma segura a las funcionalidades de biciGO.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>7</b></td>
    <td valign="top" align="center"><b>US-11</b></td>
    <td valign="top">Inicio de alquiler</td>
    <td valign="top">Como usuario registrado , quiero iniciar el alquiler de una bicicleta disponible, para utilizarla durante mi desplazamiento.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>8</b></td>
    <td valign="top" align="center"><b>US-12</b></td>
    <td valign="top">Desbloqueo de bicicleta</td>
    <td valign="top">Como usuario con un alquiler autorizado , quiero desbloquear la bicicleta mediante el mecanismo proporcionado por biciGO, para comenzar mi recorrido.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>9</b></td>
    <td valign="top" align="center"><b>US-13</b></td>
    <td valign="top">Consulta del viaje activo</td>
    <td valign="top">Como usuario con un alquiler activo , quiero consultar la información de mi recorrido, para conocer el estado actual de mi viaje.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>10</b></td>
    <td valign="top" align="center"><b>US-14</b></td>
    <td valign="top">Consulta de costo durante el viaje</td>
    <td valign="top">Como usuario con un alquiler activo , quiero consultar el costo acumulado del recorrido, para controlar cuánto estoy gastando mientras utilizo la bicicleta.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>11</b></td>
    <td valign="top" align="center"><b>US-15</b></td>
    <td valign="top">Finalización de alquiler</td>
    <td valign="top">Como usuario con un alquiler activo , quiero finalizar correctamente mi alquiler, para detener el cobro y liberar la bicicleta para otros usuarios.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>12</b></td>
    <td valign="top" align="center"><b>US-16</b></td>
    <td valign="top">Registro de método de pago</td>
    <td valign="top">Como usuario registrado , quiero registrar un método de pago, para poder pagar los servicios utilizados en biciGO.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>13</b></td>
    <td valign="top" align="center"><b>US-18</b></td>
    <td valign="top">Pago del alquiler</td>
    <td valign="top">Como usuario , quiero pagar el importe generado por mi alquiler, para completar correctamente la transacción del servicio utilizado.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>14</b></td>
    <td valign="top" align="center"><b>US-37</b></td>
    <td valign="top">Consulta de comprobantes de pago</td>
    <td valign="top">Como usuario registrado , quiero consultar los comprobantes de mis pagos realizados, para revisar los cargos asociados a mis alquileres y suscripciones.</td>
    <td valign="top" align="center"><b>2</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>15</b></td>
    <td valign="top" align="center"><b>US-06</b></td>
    <td valign="top">Permitir acceso a ubicación</td>
    <td valign="top">Como usuario registrado , quiero permitir que biciGO acceda a mi ubicación, para identificar bicicletas disponibles cercanas.</td>
    <td valign="top" align="center"><b>2</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>16</b></td>
    <td valign="top" align="center"><b>US-09</b></td>
    <td valign="top">Búsqueda de bicicletas por zona</td>
    <td valign="top">Como usuario registrado , quiero buscar bicicletas en una zona específica, para planificar un desplazamiento aunque no me encuentre actualmente en ese lugar.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>17</b></td>
    <td valign="top" align="center"><b>US-10</b></td>
    <td valign="top">Actualización de disponibilidad</td>
    <td valign="top">Como usuario registrado , quiero actualizar la disponibilidad de bicicletas mostrada, para consultar información reciente antes de seleccionar una unidad.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>18</b></td>
    <td valign="top" align="center"><b>US-23</b></td>
    <td valign="top">Consulta de historial de viajes</td>
    <td valign="top">Como usuario registrado , quiero consultar mis viajes anteriores, para revisar el uso que he realizado de biciGO.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>19</b></td>
    <td valign="top" align="center"><b>US-24</b></td>
    <td valign="top">Consulta de detalle de viaje</td>
    <td valign="top">Como usuario registrado , quiero consultar el detalle de un viaje realizado, para conocer su duración, distancia y costo final.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>20</b></td>
    <td valign="top" align="center"><b>US-26</b></td>
    <td valign="top">Reporte de bicicleta dañada</td>
    <td valign="top">Como usuario , quiero reportar una bicicleta que presente daños, para evitar que otros usuarios utilicen una unidad potencialmente insegura.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>21</b></td>
    <td valign="top" align="center"><b>US-27</b></td>
    <td valign="top">Reporte de problema durante un viaje</td>
    <td valign="top">Como usuario con un alquiler activo , quiero reportar un problema ocurrido durante mi recorrido, para recibir asistencia y dejar constancia del incidente.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>22</b></td>
    <td valign="top" align="center"><b>US-28</b></td>
    <td valign="top">Contacto con soporte</td>
    <td valign="top">Como usuario , quiero comunicarme con soporte desde la plataforma, para obtener ayuda ante problemas relacionados con mi cuenta o alquileres.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>23</b></td>
    <td valign="top" align="center"><b>US-29</b></td>
    <td valign="top">Seguimiento de incidencias</td>
    <td valign="top">Como usuario , quiero consultar el estado de mis incidencias reportadas, para conocer si están pendientes, en revisión o resueltas.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>24</b></td>
    <td valign="top" align="center"><b>US-30</b></td>
    <td valign="top">Recepción de notificaciones</td>
    <td valign="top">Como usuario , quiero recibir notificaciones relacionadas con mis alquileres, pagos e incidencias, para mantenerme informado sobre eventos importantes de mi cuenta.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>25</b></td>
    <td valign="top" align="center"><b>US-19</b></td>
    <td valign="top">Suscripción a plan mensual</td>
    <td valign="top">Como usuario frecuente , quiero contratar un plan mensual de biciGO, para acceder a condiciones de uso más convenientes.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>26</b></td>
    <td valign="top" align="center"><b>US-20</b></td>
    <td valign="top">Cancelación de suscripción</td>
    <td valign="top">Como usuario suscrito , quiero cancelar mi suscripción mensual, para evitar futuras renovaciones cuando ya no desee utilizar el plan.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>27</b></td>
    <td valign="top" align="center"><b>US-38</b></td>
    <td valign="top">Configuración de notificaciones</td>
    <td valign="top">Como usuario registrado , quiero configurar qué notificaciones deseo recibir, para controlar los avisos enviados por biciGO.</td>
    <td valign="top" align="center"><b>2</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>28</b></td>
    <td valign="top" align="center"><b>US-21</b></td>
    <td valign="top">Consulta de perfil</td>
    <td valign="top">Como usuario registrado , quiero consultar la información de mi perfil, para verificar los datos asociados a mi cuenta.</td>
    <td valign="top" align="center"><b>2</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>29</b></td>
    <td valign="top" align="center"><b>US-22</b></td>
    <td valign="top">Edición de perfil</td>
    <td valign="top">Como usuario registrado , quiero modificar mis datos personales, para mantener actualizada la información de mi cuenta.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>30</b></td>
    <td valign="top" align="center"><b>US-25</b></td>
    <td valign="top">Cambio de contraseña</td>
    <td valign="top">Como usuario registrado , quiero cambiar mi contraseña desde mi perfil, para mantener segura mi cuenta.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>31</b></td>
    <td valign="top" align="center"><b>US-36</b></td>
    <td valign="top">Eliminación de método de pago</td>
    <td valign="top">Como usuario registrado , quiero eliminar un método de pago que ya no utilizo, para mantener actualizadas mis opciones de cobro.</td>
    <td valign="top" align="center"><b>2</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>32</b></td>
    <td valign="top" align="center"><b>US-40</b></td>
    <td valign="top">Desactivación de cuenta</td>
    <td valign="top">Como usuario registrado , quiero desactivar mi cuenta cuando ya no desee utilizar biciGO, para dejar de acceder a los servicios de la plataforma.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>33</b></td>
    <td valign="top" align="center"><b>US-31</b></td>
    <td valign="top">Visualización de flota</td>
    <td valign="top">Como administrador , quiero consultar el estado de las bicicletas de la plataforma, para supervisar la disponibilidad general de la flota.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>34</b></td>
    <td valign="top" align="center"><b>US-32</b></td>
    <td valign="top">Actualización del estado de bicicleta</td>
    <td valign="top">Como administrador , quiero modificar el estado operativo de una bicicleta, para controlar qué unidades pueden ser alquiladas por los usuarios.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>35</b></td>
    <td valign="top" align="center"><b>US-33</b></td>
    <td valign="top">Gestión de incidencias de bicicletas</td>
    <td valign="top">Como administrador , quiero revisar los reportes relacionados con bicicletas dañadas, para priorizar su mantenimiento y mantener segura la flota.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>36</b></td>
    <td valign="top" align="center"><b>US-34</b></td>
    <td valign="top">Consulta de métricas de alquiler</td>
    <td valign="top">Como administrador , quiero visualizar métricas de uso de las bicicletas, para analizar el comportamiento del servicio y apoyar decisiones operativas.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>37</b></td>
    <td valign="top" align="center"><b>US-35</b></td>
    <td valign="top">Gestión de usuarios</td>
    <td valign="top">Como administrador , quiero consultar y gestionar las cuentas de los usuarios, para atender situaciones que puedan afectar la seguridad o el correcto funcionamiento de biciGO.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>38</b></td>
    <td valign="top" align="center"><b>US-03</b></td>
    <td valign="top">Recuperación de contraseña</td>
    <td valign="top">Como usuario registrado , quiero recuperar el acceso a mi cuenta cuando olvide mi contraseña, para poder continuar utilizando biciGO.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>39</b></td>
    <td valign="top" align="center"><b>US-04</b></td>
    <td valign="top">Verificación de cuenta</td>
    <td valign="top">Como usuario recién registrado , quiero verificar mi cuenta, para confirmar mis datos y habilitar el acceso completo a los servicios de biciGO.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>40</b></td>
    <td valign="top" align="center"><b>US-05</b></td>
    <td valign="top">Cierre de sesión</td>
    <td valign="top">Como usuario autenticado , quiero cerrar mi sesión, para evitar que otras personas accedan a mi cuenta desde el mismo dispositivo.</td>
    <td valign="top" align="center"><b>1</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>41</b></td>
    <td valign="top" align="center"><b>TS-05</b></td>
    <td valign="top">Get Nearby Bikes</td>
    <td valign="top">Como desarrollador , quiero implementar la consulta de bicicletas cercanas, para mostrar al usuario las unidades disponibles según su ubicación.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>42</b></td>
    <td valign="top" align="center"><b>TS-06</b></td>
    <td valign="top">Get Bike Detail</td>
    <td valign="top">Como desarrollador , quiero implementar el detalle de una bicicleta, para exponer su estado y datos necesarios antes de iniciar un alquiler.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>43</b></td>
    <td valign="top" align="center"><b>TS-07</b></td>
    <td valign="top">Search Coverage Zone</td>
    <td valign="top">Como desarrollador , quiero implementar la consulta de zonas de cobertura, para indicar si biciGO opera en una ubicación determinada.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>44</b></td>
    <td valign="top" align="center"><b>TS-01</b></td>
    <td valign="top">Register Passenger</td>
    <td valign="top">Como desarrollador , quiero implementar el endpoint de registro de usuario, para permitir la creación de cuentas en la plataforma.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>45</b></td>
    <td valign="top" align="center"><b>TS-02</b></td>
    <td valign="top">Login User</td>
    <td valign="top">Como desarrollador , quiero implementar el endpoint de inicio de sesión, para autenticar usuarios y permitir el acceso seguro a las funciones privadas.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>46</b></td>
    <td valign="top" align="center"><b>TS-08</b></td>
    <td valign="top">Start Rental</td>
    <td valign="top">Como desarrollador , quiero implementar el endpoint para iniciar un alquiler, para asociar una bicicleta disponible con un usuario autenticado.</td>
    <td valign="top" align="center"><b>8</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>47</b></td>
    <td valign="top" align="center"><b>TS-09</b></td>
    <td valign="top">Unlock Bike</td>
    <td valign="top">Como desarrollador , quiero implementar la validación del código de desbloqueo, para autorizar únicamente la apertura de la bicicleta asociada al alquiler vigente.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>48</b></td>
    <td valign="top" align="center"><b>TS-10</b></td>
    <td valign="top">Get Active Rental</td>
    <td valign="top">Como desarrollador , quiero implementar la consulta del alquiler activo, para mostrar al usuario la información actual de su viaje.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>49</b></td>
    <td valign="top" align="center"><b>TS-11</b></td>
    <td valign="top">Finish Rental</td>
    <td valign="top">Como desarrollador , quiero implementar el endpoint de finalización de alquiler, para cerrar el viaje, calcular el importe y liberar la bicicleta.</td>
    <td valign="top" align="center"><b>8</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>50</b></td>
    <td valign="top" align="center"><b>TS-12</b></td>
    <td valign="top">Register Payment Method</td>
    <td valign="top">Como desarrollador , quiero implementar el registro de métodos de pago, para permitir que los usuarios dispongan de una opción válida para realizar cobros.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>51</b></td>
    <td valign="top" align="center"><b>TS-13</b></td>
    <td valign="top">Process Rental Payment</td>
    <td valign="top">Como desarrollador , quiero implementar el procesamiento del pago de un alquiler, para registrar el cobro correspondiente al servicio utilizado.</td>
    <td valign="top" align="center"><b>8</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>52</b></td>
    <td valign="top" align="center"><b>TS-14</b></td>
    <td valign="top">Manage Subscription</td>
    <td valign="top">Como desarrollador , quiero implementar la gestión de suscripciones, para permitir activar y cancelar planes mensuales de biciGO.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>53</b></td>
    <td valign="top" align="center"><b>TS-15</b></td>
    <td valign="top">Get User Profile</td>
    <td valign="top">Como desarrollador , quiero implementar la consulta y actualización del perfil, para permitir que cada usuario gestione sus datos personales.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>54</b></td>
    <td valign="top" align="center"><b>TS-16</b></td>
    <td valign="top">Get Travel History</td>
    <td valign="top">Como desarrollador , quiero implementar la consulta del historial de viajes, para mostrar únicamente los alquileres pertenecientes al usuario autenticado.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>55</b></td>
    <td valign="top" align="center"><b>TS-17</b></td>
    <td valign="top">Create Incident</td>
    <td valign="top">Como desarrollador , quiero implementar el registro de incidencias, para almacenar reportes relacionados con bicicletas y viajes.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>56</b></td>
    <td valign="top" align="center"><b>TS-18</b></td>
    <td valign="top">Get Incident Status</td>
    <td valign="top">Como desarrollador , quiero implementar la consulta del estado de incidencias, para que el usuario pueda dar seguimiento a sus reportes.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>57</b></td>
    <td valign="top" align="center"><b>TS-19</b></td>
    <td valign="top">Manage Bike Status</td>
    <td valign="top">Como desarrollador , quiero implementar endpoints administrativos para actualizar el estado de las bicicletas, para controlar disponibilidad y mantenimiento de la flota.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>58</b></td>
    <td valign="top" align="center"><b>TS-20</b></td>
    <td valign="top">Get Dashboard Metrics</td>
    <td valign="top">Como desarrollador , quiero implementar las consultas del dashboard administrativo, para obtener métricas de alquileres, usuarios y disponibilidad de bicicletas.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>59</b></td>
    <td valign="top" align="center"><b>TS-03</b></td>
    <td valign="top">Recover Password</td>
    <td valign="top">Como desarrollador , quiero implementar el proceso de recuperación de contraseña, para que un usuario pueda restablecer sus credenciales de forma segura.</td>
    <td valign="top" align="center"><b>5</b></td>
  </tr>
  <tr>
    <td valign="top" align="center"><b>60</b></td>
    <td valign="top" align="center"><b>TS-04</b></td>
    <td valign="top">Verify Account</td>
    <td valign="top">Como desarrollador , quiero implementar la verificación de cuenta, para habilitar únicamente usuarios que hayan completado correctamente el proceso de validación.</td>
    <td valign="top" align="center"><b>3</b></td>
  </tr>
</table>
