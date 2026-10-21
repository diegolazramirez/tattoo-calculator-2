# Diegolaz Tattoo 1.0

Base Android del gestor de tatuajes de Diegolaz Ramirez.

## Este bloque incorpora

- Room como base de datos persistente para clientes y citas.
- DataStore para preferencias y configuración de la app.
- Arquitectura separada para que la interfaz no acceda directamente a la base de datos.
- Configuración persistente de precios y apariencia.
- Preparación para sincronización y copias de seguridad.
- Estructura preparada para crecer hacia cotizaciones, imágenes, consentimiento, exportaciones y Google Drive.

## Decisiones de arquitectura

Los datos grandes y relacionados (clientes, citas, etc.) usan Room; las preferencias pequeñas usan DataStore. Esto sigue las recomendaciones actuales de Android para separar la capa de UI de la capa de datos y mantener una única fuente de verdad. Consulte la documentación oficial de Android Architecture, Room y DataStore para la implementación y evolución del proyecto.

## Importante

Esta versión es código fuente. La configuración de Google OAuth/Drive, almacenamiento seguro de archivos, cifrado de base de datos y publicación requieren configuración y pruebas en un entorno Android real antes de considerarlos producción.
