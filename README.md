# Política de privacidad de Photo Path Gallery

**Responsable:** Dr. Samnir Enriquez Maciel (León, Guanajuato, México)
**Contacto:** md.samem@gmail.com
**Última actualización:** 18 de noviembre de 2026
**Versión de la app a la que aplica:** 4.13.0

## Resumen

Photo Path Gallery es una galería y herramienta de documentación fotográfica para tu teléfono Android, pensada para fotos personales y profesionales (incluidas imágenes de patología).

- **Tus fotografías y tus datos se quedan en tu teléfono.** El desarrollador no tiene servidores, no tiene cuentas de usuario y **no recibe tus fotos ni tus datos**.
- La app **no tiene publicidad** ni rastreadores propios.
- Solo se conecta a internet en dos casos: (1) si **tú activas** el asistente opcional de ChatGPT y confirmas cada envío; (2) las bibliotecas de Google ML Kit que usa la app pueden enviar estadísticas técnicas (ver «Servicios de terceros»).
- **No es un dispositivo médico y no hace diagnósticos.**

## Qué datos usa la app y para qué

| Dato | Para qué | ¿Sale del teléfono? |
|---|---|---|
| Tus fotografías y videos (nombre, fecha, tamaño, carpeta) | Mostrar, organizar, buscar, renombrar y editar tu galería | No |
| Metadatos EXIF de las fotos (cámara, fecha, ajustes) | Mostrarlos y, si lo eliges, conservarlos o eliminarlos en las copias | No |
| Ubicación GPS guardada dentro de las fotos | Solo si la pides y concedes el permiso «acceso a la ubicación de tus fotos». La app **no usa el GPS del teléfono** ni rastrea tu ubicación | No |
| Cámara y micrófono | Tomar fotos y grabar video con la cámara de la app (el micrófono, solo al grabar video con sonido o al dictar) | No (ver «Dictado por voz») |
| Datos que escribes: categorías, álbumes, etiquetas, descripciones, lugares, fichas profesionales (código, órgano, tinción, aumento, descripciones), plantillas, logotipos, textos de la marca de captura, calibraciones, casos y resultados de exámenes de docencia | Organizar, editar y exportar | No |
| Notificaciones | Mostrar el progreso de la edición por lotes | No |
| Clave de API de OpenAI (solo si la escribes) | Conectarte a ChatGPT con tu propia cuenta | Solo viaja a OpenAI al enviar una consulta |

## Dónde se guardan

- **Base de datos y ajustes**, en el almacenamiento privado de la app: organización, fichas y casos, plantillas, historial de ediciones y calibraciones.
- **Copias editadas y exportadas**, en `Pictures/Photo Path` del almacenamiento compartido, para que las veas y compartas. Como cualquier foto de tu galería, **otras apps con permiso de fotos pueden verlas**.
- **Fotos originales:** permanecen donde estaban. La app solo las lee. Solo las modifica si **tú lo pides** (renombrar, enviar a la papelera o «Quitar ubicación del original»; ver más abajo) y Android te pide confirmación.
- **Caché temporal** (miniaturas y copias para compartir), en la carpeta privada de la app. Las copias para compartir se borran automáticamente con el tiempo.
- **Registro del último cierre inesperado**, solo en tu teléfono. Contiene únicamente datos técnicos (sin texto clínico ni nombres de archivo). Nunca se envía; tú decides si lo copias.

## Funciones de privacidad

- **Baúl secreto:** guarda fotos **cifradas** (AES-256-GCM) en el almacenamiento privado de la app. Se abre con la huella, el rostro o el PIN de tu teléfono. Mientras el baúl está abierto la pantalla no admite capturas.
- **Bloqueo de la app (opcional):** pide el desbloqueo del teléfono al abrir la app o tras un tiempo en segundo plano. La app no guarda tu PIN ni tus huellas: las gestiona Android.
- **Quitar ubicación (GPS) del original (opcional):** borra solo las etiquetas GPS del archivo original de las fotos JPEG que elijas, con confirmación de Android. Antes de hacerlo, la app guarda una copia con la ubicación original en su carpeta privada (sin cifrar) para poder devolverla; tú puedes **borrar esas copias** en Ajustes. Si el cambio falla en una foto, se restaura automáticamente.
- **Anonimización y exportación para docencia:** elimina EXIF y GPS de las copias, oculta zonas y exporta con un código de caso. **No puede detectar nombres escritos como texto libre dentro de la imagen o en tus notas**: revisa siempre el resultado.
- **Detección de rostros:** se usa solo para difuminar rostros en el teléfono. No hay reconocimiento facial, no se identifica a nadie y no se guardan datos de rostros.

## Con quién se comparten

Con nadie, salvo en estos casos que **tú inicias**:

1. **Compartir** (botón de compartir): eliges una app (por ejemplo WhatsApp o correo) y a partir de ahí aplican las políticas de esa app.
2. **ChatGPT (opcional)**, descrito abajo.

## Conexión opcional con ChatGPT (OpenAI)

- Viene **apagada**. Solo funciona si en Ajustes → ChatGPT escribes **tu propia clave** de OpenAI.
- Guardamos tu clave **cifrada** con el almacén seguro de Android. No se incluye en respaldos ni se muestra completa. Puedes borrarla cuando quieras.
- Antes de cada envío la app **te muestra exactamente lo que se enviará** y debes confirmar. Se envía:
  - los datos técnicos de la ficha (tipo de imagen, procedimiento, órgano, tinción, aumento, medidas, inmunohistoquímica) y el texto que quieres redactar;
  - si eliges la opción de describir la imagen, una versión reducida de la foto **sin metadatos** (sin GPS, fecha, dispositivo ni nombre de archivo).
- **Nunca** se envían el código de estudio, el médico o servicio, el nombre del archivo, la fecha ni la ubicación.
- Lo enviado se procesa en los servidores de OpenAI conforme a sus condiciones y su política de privacidad. El desarrollador no recibe ni guarda esas consultas.
- **No envíes datos que identifiquen a un paciente.** Las respuestas de ChatGPT son **borradores** generados por inteligencia artificial: pueden contener errores, **no son un diagnóstico** y debes revisarlos antes de usarlos. Si recibes una respuesta incorrecta u ofensiva puedes descartarla; puedes reportarla con el botón **Reportar** de la pantalla del borrador: se abre un correo ya preparado hacia el desarrollador (md.samem@gmail.com) que **tú revisas y envías**; contiene solo la respuesta de la IA, la tarea y la versión de la app, nunca la ficha, la imagen ni datos del paciente.

## Dictado por voz

Al usar el micrófono para dictar, la app pide el reconocimiento de voz al servicio de Android de tu teléfono (normalmente el de Google). El audio lo procesa ese servicio según su propia política, y Photo Path Gallery solo recibe el texto. La app no graba ni guarda ese audio.

## Servicios de terceros

- **Google ML Kit** (detección de rostros y recorte de fondo): los modelos van **dentro de la app** y se ejecutan en tu teléfono; las fotos no se envían a Google. Estas bibliotecas pueden enviar a Google estadísticas técnicas de uso y rendimiento (por ejemplo, versión de la biblioteca, tipo de dispositivo y errores) según la política de Google ML Kit.
- **OpenAI**, solo si activas ChatGPT.
- La app **no incluye** publicidad, análisis de comportamiento, Firebase Analytics ni reportes de fallos en la nube.

## Copias de seguridad

- La copia de seguridad en la nube de Google para esta app está **desactivada**.
- Al pasar a un teléfono nuevo con la transferencia directa de Android, la organización de la app puede copiarse al nuevo teléfono.
- **Exportar respaldo** crea un archivo en el lugar que elijas. Puede protegerse con **contraseña** (cifrado AES-256-GCM). **Sin contraseña queda sin cifrar** y puede incluir datos profesionales (por ejemplo, códigos de caso) y logotipos: guárdalo en un lugar seguro. Si olvidas la contraseña, no se puede recuperar. Las fotos no se incluyen en el respaldo.
- Antes de restaurar un respaldo, la app guarda una copia de seguridad automática (sin cifrar) en su carpeta privada.

## Fotografías médicas y responsabilidad

Photo Path Gallery **no es un dispositivo médico**, no diagnostica ni sustituye el juicio de un profesional de la salud. Para fotos con datos de pacientes ofrece herramientas para eliminar EXIF y GPS, ocultar zonas y exportar con un código de caso. **Tú eres responsable** de contar con el consentimiento necesario, de proteger la información de tus pacientes y de cumplir la normativa que te aplique (en México, por ejemplo, la Ley Federal de Protección de Datos Personales en Posesión de los Particulares y las normas sobre expediente clínico). Las estadísticas de la app son conteos de lo que tú capturaste, no interpretaciones.

## Cuánto tiempo se conservan y cómo eliminarlos

- Los datos se conservan en tu teléfono hasta que los borres.
- Dentro de la app puedes eliminar fotos (van a la papelera de Android unos 30 días), categorías, álbumes, etiquetas, plantillas, logotipos, casos, la clave de ChatGPT, las copias de recuperación de GPS y los datos de análisis de Photo Path Vision.
- **Desinstalar la app** o usar **Ajustes de Android → Apps → Photo Path Gallery → Borrar datos** elimina la base de datos, los ajustes, el baúl cifrado y las copias privadas.
- **No se borran** al desinstalar las fotos originales ni las copias de `Pictures/Photo Path`: bórralas desde tu galería si ya no las quieres.
- Como el desarrollador no recibe ni guarda tus datos, no tiene datos tuyos que corregir o eliminar. Para lo que enviaste a OpenAI, consulta sus políticas.

## Menores de edad

La app está dirigida a personas de **18 años o más** y no recopila a sabiendas datos de menores.

## Cambios a esta política

Si una versión futura cambia el tratamiento de datos, esta política y la sección «Seguridad de los datos» de Google Play se actualizarán **antes** de publicar esa versión. La fecha de arriba indica la última revisión.

## Contacto

Dr. Samnir Enriquez Maciel · md.samem@gmail.com · León, Guanajuato, México
