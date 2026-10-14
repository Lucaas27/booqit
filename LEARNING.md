# Booqit learning tracker

Build an event discovery and ticketing API while learning the .NET Web API concepts in the [Zero to Hero course](https://codewithmukesh.com/courses/dotnet-webapi-zero-to-hero/lessons/). The learner writes the code; guidance should explain the idea, give a small task, and help verify the result.

## Roadmap

- [ ] **1. HTTP and REST foundations** — create/run the API; request/response flow, resources and routes, HTTP methods, status codes, OpenAPI.
- [ ] **2. ASP.NET Core foundations** — configuration, dependency injection and lifetimes, middleware, validation, Problem Details, logging.
- [ ] **3. Events and venues** — EF Core, entities and relationships, migrations, CRUD, pagination/search/sorting.
- [ ] **4. Accounts and authorization** — authentication, roles/policies, organizer and attendee permissions.
- [ ] **5. Ticket reservations** — booking model, transactions, inventory and optimistic concurrency to prevent overbooking.
- [ ] **6. Safe retries** — idempotency keys for reservation/checkout POSTs; replay the original result, scope keys to the caller, reject changed payloads, and handle concurrent duplicate requests.
- [ ] **7. Production practices** — tests, rate limiting, caching, background expiration of unpaid reservations, health checks and observability.
- [ ] **8. Delivery** — Docker and CI/CD. Add external payments, webhooks, or real-time availability only if useful.

## Session log

### Session 0 — project and learning approach

- Chosen project: event discovery and ticketing API (Booqit).
- Keep beginner material; explain concepts while applying them to the project.
- Build manually: do not generate the application implementation on the learner's behalf.
- Idempotency is a specific learning goal, especially safe booking retries.
- Project created: `Booqit.API`, ASP.NET Core Web API targeting .NET 10, using the controller-based template. It currently has the template `WeatherForecastController`, OpenAPI endpoint, and a `.http` request file.
- Progress: API ran and the weather request returned a JSON array with `200 OK`. Headers and route-to-controller flow still need discussion; HTTP/REST foundations remain in progress.

### Session 1 — first request

- User ran the template API and received five forecast objects as JSON.
- User confirmed the response status was `200 OK`.
- Response headers observed: `Content-Type: application/json; charset=utf-8`, `Server: Kestrel`, and `Transfer-Encoding: chunked`.
- Values are generated for each request; `TemperatureF` is calculated from `TemperatureC`, while `Date` serializes as `YYYY-MM-DD` and C# property names serialize as camelCase.

## Resume here

**Next:** design the first Booqit endpoint before coding: propose its HTTP method and URL, the JSON fields in its response, and the status code for success. Start with listing public events; then discuss the resource-oriented choices and map it to a controller route.

At the start of a session, read this file and inspect the current repository. After a session, update the checkboxes, session log, and next step. In a new chat, share this file and the repository path: `/Users/lucasgomes/Documents/projects/Booqit`.
