# Tattoo Manager Calculator — 1.5 Audited

Aplicación Android para gestión de tatuadores. Perfil inicial: Diegolaz Ramirez.

## Cambios de esta auditoría
- Se eliminó la regla fija 2x1: las promociones son creadas por cada tatuador.
- Paquetes configurables (2 por 1, 3 por 1, etc.), descuento porcentual y descuento fijo.
- Se añadió recargo porcentual configurable por zona, además del estilo.
- La cotización permite decidir si la cita se agrega realmente a la agenda; ya no crea una cita automáticamente con la hora actual.
- Se añadieron fecha/hora de cita y abono a la cotización.
- Exportación PDF y compartir cotización como texto.
- Se añadió calculadora de costos con tinta, vida útil de máquina, termocopiadora, insumos y otros costos porcentuales.
- Se mejoró la seguridad del PIN usando PBKDF2 con sal en vez de SHA-256 simple.
- Se añadió activación real del interruptor de biometría.
- Se usa OpenMultipleDocuments para conservar permisos de lectura de imágenes seleccionadas.
- Se añadió acceso rápido a llamada, WhatsApp e Instagram desde el cliente.
- Se solicita permiso de notificaciones en Android 13+.
- Se eliminaron implementaciones duplicadas de motor de cotización y preferencias que podían divergir de la lógica real.
- Apariencia: fondo, acento, texto y tamaño de fuente configurables.

## Pendiente de producción
- Compilar con Android Studio/SDK y ejecutar pruebas en teléfonos y tablets reales.
- Completar traducción de todos los textos de UI a español/inglés/portugués. El selector y configuración de idioma están preparados, pero la localización completa de cada pantalla debe probarse con recursos Android.
- Implementar Google OAuth/Drive real y copias de seguridad cifradas extremo a extremo.
- Exportación de imágenes PNG/JPG y DOCX nativo; PDF ya tiene implementación.
- Migrar el repositorio JSON local a una base de datos Room cuando se defina el esquema final de cotizaciones, pagos e imágenes.
- Revisar consentimiento y tratamiento de datos sensibles con asesoría legal local antes de publicación.

Esta versión es código fuente y no ha sido compilada en este entorno por no disponer del Android SDK/Gradle toolchain.
