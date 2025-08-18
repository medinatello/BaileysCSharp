# Flujos unificados

## Tabla de contenidos
- [Conectar y autenticar](#conectar-y-autenticar)
- [Enviar mensaje](#enviar-mensaje)
- [Errores y reintentos](#errores-y-reintentos)
- [Proveniencia](#proveniencia)

## Conectar y autenticar
```mermaid
sequenceDiagram
    participant C as Cliente
    participant W as WASocket
    participant S as Servidor WA
    C->>W: Configurar
    W->>S: Handshake
    S-->>W: Challenge
    W-->>S: Credenciales
    S-->>W: Sesión activa
```

## Enviar mensaje
```mermaid
sequenceDiagram
    C->>W: sendMessage()
    W->>S: Frame binario
    S-->>W: Ack
    W-->>C: Evento de confirmación
```

## Errores y reintentos
- Reintentar conexión ante códigos de cierre temporales.
- Registrar timeouts superiores a 30s.

## Proveniencia
- [Codex flujos](../DocumentationCodex/04-flujos-tecnicos.md)
- [Jules flujos](../DocumentationJules/04-flujos-tecnicos.md)
