# Arquitectura unificada

## Tabla de contenidos
- [Diagrama general](#diagrama-general)
- [Componentes y dependencias](#componentes-y-dependencias)
- [Divergencias](#divergencias)
- [Proveniencia](#proveniencia)

## Diagrama general
```mermaid
graph TD
    subgraph "Capa de Aplicación"
        A[WhatsSocketConsole]
    end
    subgraph "Librería BaileysCSharp"
        B(WASocket)
        C{EventEmitter}
        D[Cliente WebSocket]
        E[Handlers]
        F[Persistencia]
        G[Criptografía]
    end
    subgraph "Dependencias Externas"
        H[Servidores WhatsApp]
        I[LiteDB]
        J[BouncyCastle]
    end
    A -->|Configura| B
    B -->|Eventos| C
    B -->|Conecta| D
    D -->|Frames| H
    D -->|Datos| E
    E -->|Claves| G
    E -->|Estado| F
```

## Componentes y dependencias
- `WASocket` como fachada de operaciones.
- `EventEmitter` difunde cambios de estado.
- Persistencia mediante LiteDB y archivos.
- Criptografía basada en BouncyCastle/LibSignal.

## Divergencias
- Codex destaca una cadena de sockets especializada.
- Copilot describe patrones adicionales como Observer y Factory.

## Proveniencia
- [Codex](../DocumentationCodex/02-arquitectura-actual.md)
- [Jules](../DocumentationJules/02-arquitectura-actual.md)
- [Copilot](../DocumentationCopilot/02-arquitectura-actual.md)
