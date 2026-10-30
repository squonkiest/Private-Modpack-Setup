# Components

Each reusable component is its own .NET project. The backend may reference
these projects, but component projects must not reference anything under
`apps/backend`.

Current projects:

- `providers` — external mod platform data access.
- `modpack` — manifest handling, resolution, and caching.
- `installer` — client installation preparation.
- `instance-manager` — dedicated server container lifecycle.

Keep components independent until a concrete shared dependency is needed.
