# QA Audit — Tattoo Manager Calculator 1.5

## Hallazgos corregidos
1. La promoción 2x1 estaba tratada como regla especial. Ahora es una promoción configurable.
2. La cotización guardaba una cita con la fecha/hora actuales aunque el usuario no lo pidiera. Ahora existe `Agregar esta cotización a la agenda` y fecha/hora explícitas.
3. Las zonas no tenían porcentajes configurables. Ahora tienen recargos editables.
4. La biometría se mostraba como estado pero no podía activarse desde Ajustes. Ahora tiene Switch.
5. El PIN usaba SHA-256 sin sal. Se reemplazó por PBKDF2-HMAC-SHA256 con sal aleatoria.
6. Las imágenes usaban un selector que no garantizaba persistencia de permisos. Ahora usa OpenMultipleDocuments y solicita permiso persistente cuando Android lo permite.
7. No había calculadora de costos funcional en la navegación. Se añadió.
8. No había exportación PDF desde la cotización. Se añadió.
9. No había acciones de contacto. Se añadieron llamada, WhatsApp e Instagram.
10. Las preferencias de color/texto estaban parcialmente desconectadas de la interfaz. Ahora el tema usa fondo, acento y texto configurados.

## Riesgos que requieren prueba real
- Compilación y ejecución en Android Studio.
- Android 13+ notificaciones y restricciones de batería/alarmas.
- Restauración de permisos de URI después de reinicio.
- Migración de datos de versiones anteriores.
- Google OAuth/Drive.
- Exportaciones y compatibilidad de documentos.
- Accesibilidad, tablet, orientación y tamaños de fuente extremos.
