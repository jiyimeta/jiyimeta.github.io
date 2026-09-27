---
layout: page
locale: es
kind: folino-privacy
permalink: /folino/privacy-policy/es/
---
# Política de privacidad de folino

Última actualización: 27 de septiembre de 2026

Esta Política de privacidad describe cómo folino, la aplicación de partituras proporcionada por Harmolo (en adelante, «nosotros»), gestiona la información en iPhone, iPad, Mac y Android. Las demás aplicaciones de Harmolo se rigen por la [Política de privacidad de Harmolo](/privacy-policy/es/).

folino funciona sin cuenta. Leer, reproducir, editar y anotar partituras no requiere iniciar sesión, y sus partituras permanecen en su dispositivo a menos que inicie sesión. Lo que se describe a continuación en «Cuenta, sincronización y grupos compartidos» solo ocurre si usted decide iniciar sesión.

## Información que recopilamos y finalidad de uso

1. **Datos de fallos y diagnóstico**
   folino recopila información de fallos y diagnóstico —como los seguimientos de pila de los fallos, un breve registro de los pasos previos a un problema y datos estándar del dispositivo (modelo del dispositivo, versión del sistema operativo, versión de la aplicación)— mediante un servicio de informes de fallos (Firebase Crashlytics) para mejorar la estabilidad y corregir errores. El software del servicio también puede enviar señales técnicas de diagnóstico sobre su propio funcionamiento. Puede desactivar los informes de fallos en «Settings → Privacy» (Ajustes → Privacidad). Estos datos no se vinculan a su identidad.

2. **Datos de uso**
   folino recopila datos de uso, como las vistas de pantalla, las funciones utilizadas y el número de elementos, mediante un servicio de analítica (Google Analytics for Firebase) para mejorar la funcionalidad. El servicio de analítica también registra información de contexto estándar —versión de la aplicación y del sistema operativo, modelo del dispositivo, idioma, inicio y duración de la sesión— junto con un identificador de la instalación de la aplicación, y deduce una ubicación aproximada (a nivel de ciudad) a partir de la dirección de red. No se envían al servicio de analítica nombres, direcciones de correo electrónico, identificadores de cuenta ni contenido (como títulos o archivos), y estos datos no se vinculan a su identidad. Puede desactivar la analítica de uso en «Settings → Privacy» (Ajustes → Privacidad).

3. **Micrófono** (Mac)
   En el Mac, la barra de tono utiliza el micrófono para mostrar en tiempo real el tono de su voz o de su instrumento. Este audio se procesa únicamente en su dispositivo. Nunca se graba, almacena ni transmite a nosotros ni a terceros.

4. **Cuenta, sincronización y grupos compartidos** (solo si inicia sesión)
   Iniciar sesión es opcional y es lo que permite sincronizar su biblioteca entre sus dispositivos y compartir con un grupo. Si inicia sesión, recopilamos lo siguiente, y estos datos se vinculan a su cuenta:

   - **Información de la cuenta.** Puede iniciar sesión con Apple, con Google o con un enlace de inicio de sesión enviado a su dirección de correo electrónico. Recibimos un identificador de cuenta, su dirección de correo electrónico (con «Ocultar mi correo electrónico» de «Iniciar sesión con Apple», una dirección de reenvío) y, si el servicio de inicio de sesión lo proporciona o usted lo introduce, su nombre. Cuando solicita un enlace de inicio de sesión, su dirección de correo electrónico se envía a nuestro servidor, que crea el enlace y envía el correo a través de nuestro proveedor de envío de correo electrónico; conservamos un hash unidireccional de la dirección y la hora de la última solicitud, únicamente para limitar las solicitudes repetidas.
   - **Perfil.** El nombre visible que elija y, si añade una, una foto de perfil. Antes de subirlas, las fotos se redimensionan y se les eliminan los metadatos de ubicación y de cámara. Su perfil se muestra a los miembros de los grupos a los que pertenece, y otros usuarios de folino que hayan iniciado sesión y conozcan su identificador de cuenta pueden consultarlo.
   - **Sus partituras y anotaciones.** Cuando la sincronización está activada (puede desactivarla en cualquier momento en «Settings» [Ajustes]), los archivos de partituras de su biblioteca, sus datos (como el título, el compositor, el tamaño del archivo y si están marcadas como favoritas), sus anotaciones y un historial de las ediciones de notas que realiza (incluido el dispositivo desde el que se hicieron) se almacenan en la nube para que sus otros dispositivos los reciban.
   - **Grupos compartidos.** Los grupos son solo por invitación. Lo que añade a un grupo —partituras, las anotaciones que marca como compartidas, el nombre y la imagen del grupo— es visible para los miembros del grupo, junto con su nombre visible y su foto de perfil. Las anotaciones que marca como privadas se almacenan con el grupo, pero no se muestran a los demás miembros; el administrador del grupo tiene acceso técnico a ellas para que la eliminación de un grupo pueda borrarlas, y folino nunca se las muestra al administrador.
   - **Actividad en partituras compartidas y sincronizadas.** Mientras tiene abierta una partitura sincronizada o compartida, sus otros dispositivos y los miembros de ese grupo pueden ver que la está viendo o editando y dónde está su cursor. Esta información se elimina cuando cierra la partitura o se desconecta. Mientras edita una partitura sincronizada, se mantiene un bloqueo de edición de corta duración que incluye su nombre visible para que dos personas no editen al mismo tiempo.
   - **Identificador del dispositivo.** Un identificador aleatorio creado para cada instalación de la aplicación se almacena con la actividad, el bloqueo de edición y el historial de ediciones mencionados anteriormente, para poder distinguir entre sí sus propios dispositivos. No se utiliza para publicidad ni para seguimiento.
   - **Denuncias y comentarios.** Si denuncia a un miembro o un grupo, o envía comentarios, su propia aplicación de correo electrónico abre un mensaje dirigido a nosotros que contiene los identificadores necesarios para gestionarlo (por ejemplo, el grupo, el miembro y su identificador de cuenta) y la versión de la aplicación, la versión del sistema operativo y el modelo de su dispositivo. No se envía nada a menos que usted envíe ese correo electrónico.

   Utilizamos esta información únicamente para ofrecer estas funciones: el inicio de sesión, la sincronización, el uso compartido con sus grupos y la gestión de denuncias. Los datos se almacenan en nuestro proveedor de servicios en la nube y no están cifrados de extremo a extremo, por lo que son accesibles para nosotros como operador del servicio; solo accedemos a ellos cuando es necesario para operar el servicio, responder a una denuncia o cumplir la ley.

folino no muestra anuncios. No vendemos información personal ni la utilizamos para hacer seguimiento a través de aplicaciones o sitios web de otras empresas.

## Proveedores de servicios y divulgación de información personal a terceros

No compartimos información personal con terceros, salvo en los casos descritos en esta Política o cuando la ley lo exija. Los siguientes proveedores procesan datos en nuestro nombre:

- **Google (Firebase)** — inicio de sesión en la cuenta (Firebase Authentication), almacenamiento en la nube de los datos sincronizados y compartidos (Cloud Firestore, Cloud Storage, Realtime Database), funciones de servidor, comprobaciones de integridad de la aplicación (Firebase App Check), configuración, informes de fallos (Firebase Crashlytics) y analítica de uso (Google Analytics for Firebase).
- **Resend** — envío de los correos electrónicos de inicio de sesión.
- **Apple y Google** — cuando elige «Iniciar sesión con Apple» o «Iniciar sesión con Google», ese servicio gestiona su inicio de sesión conforme a su propia política de privacidad.
- **GitHub** — folino descarga sonidos de instrumentos adicionales desde GitHub, que recibe la información estándar de la solicitud, como su dirección de red.

El contenido que añade a un grupo compartido se comparte, por su propia naturaleza, con los miembros de ese grupo.

Sus datos pueden almacenarse y procesarse en países distintos del suyo, incluidos Japón, Singapur y los Estados Unidos.

## Conservación y eliminación de datos

- **Los datos de fallos y diagnóstico** se conservan en el servicio de informes de fallos durante un período limitado y luego se eliminan. Firebase Crashlytics conserva los datos de fallos durante 90 días antes de comenzar a eliminarlos de sus sistemas en producción y de copia de seguridad.
- **Los datos de uso** se conservan en el servicio de analítica durante el período de conservación que configuramos, como máximo 14 meses.
- **Los datos de la cuenta y los datos sincronizados** se conservan hasta que elimine su cuenta. El historial de ediciones de notas se elimina automáticamente unos 12 meses después de cada edición. Una partitura que mueva a «Recently Deleted» (Eliminado recientemente) se quita de sus otros dispositivos, pero su copia en el servidor se conserva hasta que elimine su cuenta.
- **Eliminación de su cuenta.** «Settings → Account → Delete Account…» (Ajustes → Cuenta → Eliminar cuenta…) elimina su cuenta junto con las partituras, anotaciones, historial de ediciones, perfil y fotos almacenados para ella, y le retira de sus grupos (un grupo del que usted era el último miembro se elimina). Las partituras que haya añadido a un grupo que siga existiendo permanecen disponibles para sus demás miembros, y las copias ya descargadas en los dispositivos de otros miembros no pueden retirarse. Eliminar su cuenta no elimina los datos de su propio dispositivo.
- También puede solicitar el acceso, la rectificación o la eliminación de los datos asociados a su uso de folino poniéndose en contacto con nosotros en la dirección de correo electrónico que figura a continuación.

## Cambios en esta Política

Podemos actualizar esta Política de privacidad cuando sea necesario. Cualquier cambio entrará en vigor una vez publicado en esta página.

## Contacto

Proveedor: Harmolo
Correo electrónico: contact@harmolo.com
