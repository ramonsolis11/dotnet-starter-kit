# .NET 9 Clean Architecture Reference

> Architecture study and reference implementation based on the open-source **FullStackHero .NET Starter Kit**.

This repository is maintained in my GitHub as a technical reference for evaluating modern .NET architecture patterns, platform capabilities and cloud-ready application design.

## Purpose

The goal of this repository is to study and validate architectural concepts that are relevant to enterprise .NET solutions, including:

- Clean Architecture and modular boundaries
- Multi-tenancy
- ASP.NET Core Web API design
- Blazor client integration
- Entity Framework Core
- PostgreSQL persistence
- Redis-based infrastructure
- Validation and request handling patterns
- Containerized local development
- Observability through .NET Aspire

## Technology Stack

- .NET 9
- ASP.NET Core Web API
- Blazor
- Entity Framework Core 9
- PostgreSQL
- Redis
- MediatR
- FluentValidation
- Docker
- .NET Aspire

## Architectural View

```text
Client / Blazor
      |
      v
ASP.NET Core API
      |
      +--> Application / Use Cases
      |
      +--> Domain
      |
      +--> Infrastructure
              |
              +--> PostgreSQL
              +--> Redis
              +--> Identity / Multi-Tenancy
```

The value of this repository is not only the technology stack, but the separation of concerns and the way cross-cutting capabilities can be integrated without coupling business logic to infrastructure concerns.

## Local Development

### Prerequisites

- .NET 9 SDK
- Visual Studio 2022+ or compatible IDE
- Docker Desktop
- PostgreSQL

### Run

1. Clone the repository.
2. Open `./src/FSH.Starter.sln`.
3. Configure the database connection in `./src/api/server/appsettings.Development.json`.
4. Run the Aspire project as the startup project.

Typical local endpoints:

- Aspire Dashboard: `https://localhost:7200/`
- API / Swagger: `https://localhost:7000/swagger/index.html`
- Blazor Client: `https://localhost:7100/`

## Engineering Topics I Evaluate Here

- Modular monolith vs distributed architecture trade-offs
- Tenant isolation strategies
- Authentication and authorization boundaries
- Data-access abstractions
- Infrastructure dependency management
- API composition
- Container-first development workflows
- Operational readiness and observability

## Attribution

This repository is based on the open-source **FullStackHero .NET Starter Kit**. The upstream project and its contributors deserve full credit for the original implementation.

Upstream project: `fullstackhero/dotnet-starter-kit`

My use of this repository is focused on architecture analysis, experimentation and reference design.

## License

See the repository license and the upstream FullStackHero project for licensing details.
