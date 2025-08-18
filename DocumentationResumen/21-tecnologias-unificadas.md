# Tecnologías unificadas

## Tabla de contenidos
- [Tabla comparativa](#tabla-comparativa)
- [Proveniencia](#proveniencia)

## Tabla comparativa
| Tecnología | Propósito | Uso actual | Problemas | Mejoras/Alternativas |
|------------|-----------|------------|-----------|----------------------|
| LiteDB | Persistencia local | Almacena chats y claves | Acoplamiento fuerte, rendimiento limitado | Introducir interfaz o evaluar SQLite/LiteDB reemplazable |
| System.Net.WebSockets | Comunicación en tiempo real | Conexión con WhatsApp Web | Manejo de errores limitado | Abstraer capa y permitir reemplazos |
| BouncyCastle / LibSignal | Criptografía | Cifrado punto a punto | Complejidad de claves | Documentar procesos y encapsular |
| Google.Protobuf | Serialización | Generación de clases WA | Complejidad de build | Precompilar y versionar proto |
| FFMpegCore / SkiaSharp | Multimedia | Procesamiento de audio/video/imágenes | Dependencias nativas | Revisar uso y encapsular servicios |

## Proveniencia
- [Codex tecnologías](../DocumentationCodex/03-tecnologias-usadas.md)
- [Jules tecnologías](../DocumentationJules/03-tecnologias-usadas.md)
- [Copilot tecnologías](../DocumentationCopilot/03-tecnologias-usadas.md)
