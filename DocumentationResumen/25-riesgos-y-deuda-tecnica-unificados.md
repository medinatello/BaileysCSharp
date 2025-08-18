# 25. Riesgos y deuda técnica unificados

- [Matriz de riesgos](#matriz-de-riesgos)
- [Deuda técnica priorizada](#deuda-técnica-priorizada)

## Matriz de riesgos
| Riesgo | Impacto | Probabilidad | Mitigación |
|--------|---------|--------------|------------|
| Robo de credenciales | Alto | Media | Cifrar `creds.json` y limpiar archivos sensibles |
| Cambios en protocolo WA | Alto | Alta | Vigilar repositorio oficial y actualizar protobuf |
| Falta de tests en refactor | Medio | Alta | TDD con cobertura mínima 70% |
| Dependencia de libs nativas | Medio | Baja | Encapsular en contenedores |

## Deuda técnica priorizada
1. `WASocket` como *God Object* con alto acoplamiento.
2. Credenciales en texto plano.
3. Ausencia de reconexión automática y manejo de errores robusto.
4. Logging no estructurado sin telemetría.

### Proveniencia
- [DocumentationCodex/09-riesgos-costos-y-deuda-tecnica.md](../DocumentationCodex/09-riesgos-costos-y-deuda-tecnica.md)
- [DocumentationJules/09-riesgos-costos-y-deuda-tecnica.md](../DocumentationJules/09-riesgos-costos-y-deuda-tecnica.md)

