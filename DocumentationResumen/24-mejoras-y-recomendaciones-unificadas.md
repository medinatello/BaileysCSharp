# 24. Mejoras y recomendaciones unificadas

- [Errores y resiliencia](#errores-y-resiliencia)
- [Logs y telemetría](#logs-y-telemetría)
- [Seguridad](#seguridad)

## Errores y resiliencia
- Definir jerarquía de excepciones (`Transient`, `Authentication`, `Protocol`).
- Implementar políticas de reintentos con Polly y propagar `CancellationToken`.

## Logs y telemetría
- Adoptar `Microsoft.Extensions.Logging` + `Serilog` con formato JSON.
- Integrar OpenTelemetry para trazas y métricas (latencia, reconexiones, tamaño de mensaje).

## Seguridad
- Cifrar `creds.json` y aplicar scrubbing de datos sensibles en logs.

### Proveniencia
- [DocumentationCodex/06-mejoras-errores-logs-telemetria.md](../DocumentationCodex/06-mejoras-errores-logs-telemetria.md)
- [DocumentationJules/06-mejoras-errores-logs-telemetria.md](../DocumentationJules/06-mejoras-errores-logs-telemetria.md)

