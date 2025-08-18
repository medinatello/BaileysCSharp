# 21. Tecnologías unificadas

- [Tabla principal](#tabla-principal)

## Tabla principal
| Tecnología | Propósito | Uso actual | Problemas | Mejoras | Alternativas |
|------------|-----------|------------|-----------|---------|--------------|
| LiteDB | Persistencia embebida de sesiones y mensajes | Guardado de chats y credenciales | Sin cifrado y acoplamiento fuerte | Abstraer mediante interfaz, evaluar SQLite | SQLite |
| System.Net.WebSockets | Transporte tiempo real | Conexión `wss://web.whatsapp.com/ws/chat` | Reconexión básica | Política de reintentos con Polly | Bibliotecas externas |
| BouncyCastle / LibSignal | Criptografía E2E | Implementación del protocolo Signal | Claves en texto plano | Envolver lógica cripto y cifrar en reposo | libsodium |
| Google.Protobuf | Serialización | Generación de clases WAProto | Código generado mezclado | Automatizar build | gRPC tools actualizados |
| FFMpegCore / SkiaSharp | Procesamiento multimedia | Transcodificación y miniaturas | Dependencias nativas pesadas | Pooling y validación de formatos | Servicios externos |

### Proveniencia
- [DocumentationCodex/03-tecnologias-usadas.md](../DocumentationCodex/03-tecnologias-usadas.md)
- [DocumentationJules/03-tecnologias-usadas.md](../DocumentationJules/03-tecnologias-usadas.md)
- [DocumentationCopilot/03-tecnologias-usadas.md](../DocumentationCopilot/03-tecnologias-usadas.md)

