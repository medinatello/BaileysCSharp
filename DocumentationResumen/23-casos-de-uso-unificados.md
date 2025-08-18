# Casos de uso unificados

## Tabla de contenidos
- [Enviar mensaje de texto](#enviar-mensaje-de-texto)
- [Descargar multimedia](#descargar-multimedia)
- [Proveniencia](#proveniencia)

## Enviar mensaje de texto
- **Como** operador
- **Quiero** enviar un mensaje a un número
- **Para** iniciar una conversación
- **Precondiciones**: sesión autenticada
- **Postcondiciones**: mensaje confirmado por el servidor
- **Criterios de aceptación**:
  - Se recibe `ack` de WhatsApp
  - Se notifica mediante evento al cliente

## Descargar multimedia
- **Como** analista
- **Quiero** descargar un archivo adjunto
- **Para** almacenarlo localmente
- **Precondiciones**: mensaje con media disponible
- **Postcondiciones**: archivo persistido en disco
- **Criterios de aceptación**:
  - El archivo existe y su tamaño es mayor a cero

## Proveniencia
- [Codex casos](../DocumentationCodex/05-casos-de-uso.md)
- [Jules casos](../DocumentationJules/05-casos-de-uso.md)
