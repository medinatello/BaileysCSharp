# 23. Casos de uso unificados

- [Establecer nueva sesión](#establecer-nueva-sesión)
- [Reconectar sesión existente](#reconectar-sesión-existente)

## Establecer nueva sesión
Como **sistema** quiero guiar a un cliente sin credenciales a través del escaneo de un código QR para establecer una sesión segura.
- **Precondiciones**: inexistencia de `creds.json`, conectividad a Internet.
- **Postcondiciones**: conexión abierta y credenciales almacenadas cifradas.
- **Criterios de aceptación**: QR disponible <2s; tasa de éxito >99%.

## Reconectar sesión existente
Como **sistema** quiero usar credenciales persistidas para reanudar rápidamente una sesión previa sin intervención del usuario.
- **Precondiciones**: archivo de credenciales válido.
- **Postcondiciones**: estado `Open` sin regenerar QR.
- **Criterios de aceptación**: reconexión automática ante cortes temporales.

### Proveniencia
- [DocumentationJules/05-casos-de-uso.md](../DocumentationJules/05-casos-de-uso.md)
- [DocumentationCodex/05-casos-de-uso.md](../DocumentationCodex/05-casos-de-uso.md)

