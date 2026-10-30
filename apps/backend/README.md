# Backend API

The backend targets .NET 10 and C# 14. Shared build settings live in
`build/Directory.Build.props`, imported by the `apps/` and `components/` trees.

## Projects

- `src/Api` — ASP.NET Core HTTP API and application composition root.
- `src/Application` — use cases and orchestration.
- `src/Domain` — core domain types and rules.
- `src/Infrastructure` — external services, persistence, and component adapters.

The API backend may depend on reusable projects under `components/`. Component
projects must not reference projects under `apps/backend/`. Within the backend,
Application depends on Domain, Infrastructure implements Application-facing
abstractions, and Api wires the projects together.

## Build and run

From the repository root:

```powershell
dotnet build .\PrivateModpackSetup.sln
dotnet run --project .\apps\backend\src\Api\PrivateModpackSetup.Api.csproj
```

The initial API exposes `GET /health` as a basic startup check.
