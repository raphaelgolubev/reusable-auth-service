# Reusable Auth Service

Generic сервис, выполняющий идентификацию, аутентификацию и авторизацию пользователей.

## Идея

Создать самостоятельный сервис, который можно встраивать в любой проект, преимущественно в проекты на микросервисной архитектуре.

Допускается возможность развертывания как отдельного микросервиса, так и возможность
встраивания в другой микросервис.

![docs/main.excalidraw.png](docs/main.excalidraw.png)

```mermaid
sequenceDiagram

participant App as Any app
participant AuthService
participant UserRepository
participant TokenService
participant UserService
participant UserRepository
participant TokenService

App->>AuthService: Incoming request
AuthService->>UserRepository: FindByUsername
```