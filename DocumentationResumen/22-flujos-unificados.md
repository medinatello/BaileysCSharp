# 22. Flujos unificados

- [Conectar y autenticar](#conectar-y-autenticar)
- [Enviar mensaje](#enviar-mensaje)
- [Recibir mensaje](#recibir-mensaje)
- [Gestionar grupos](#gestionar-grupos)
- [Cerrar conexión](#cerrar-conexión)

## Conectar y autenticar
```mermaid
sequenceDiagram
    participant App
    participant WASocket
    participant WS as WebSocketClient
    participant WA as Servidor
    App->>WASocket: new WASocket(config)
    WASocket->>WS: Connect
    WS->>WA: Handshake
    WA-->>WS: QR o credenciales
    WASocket-->>App: Evento QR/Connection.Update
```
Errores: expiración de QR, timeouts.

## Enviar mensaje
```mermaid
sequenceDiagram
    App->>WASocket: SendMessage
    WASocket->>WA: Nodo cifrado
    WA-->>WASocket: ack
    WASocket-->>App: MessageStatus
```

## Recibir mensaje
```mermaid
sequenceDiagram
    WA-->>WASocket: Frame binario
    WASocket->>WASocket: decrypt + parse
    WASocket-->>App: Message.Upsert
```

## Gestionar grupos
```mermaid
sequenceDiagram
    App->>WASocket: CreateGroup
    WASocket->>WA: iq set
    WA-->>WASocket: group id
    WASocket-->>App: Group.Update
```

## Cerrar conexión
```mermaid
sequenceDiagram
    App->>WASocket: EndConnection
    WASocket->>WA: Close frame
    WASocket-->>App: Connection.Update(disconnected)
```

### Proveniencia
- [DocumentationCodex/04-flujos-tecnicos.md](../DocumentationCodex/04-flujos-tecnicos.md)
- [DocumentationJules/04-flujos-tecnicos.md](../DocumentationJules/04-flujos-tecnicos.md)

