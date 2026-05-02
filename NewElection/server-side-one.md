# Server Side One

## Summary
Build the backend foundation for data modeling, authentication, user management, and election CRUD.

## Responsibilities
- Define core data models and schema
  - `User` with roles: `voter`, `moderator`, `administrator`, `reporter`, `super administrator`
  - `Election` with fields: `election_id`, `title`, `description`, `options`, `createdAt`, `opensAt`, `closesAt`, `owned`, `deleted`
  - `Ballot` / ranking payloads
  - Assignment relationships for voters and moderators
- Implement authentication and role-based access control
  - Require authenticated users for all views and operations
  - Enforce role access rules consistently
- Implement user management APIs
  - Create/update/delete voters, moderators, reporters
  - Allow administrator creation only by super administrator
  - Enable administrators to view deleted users
  - Prevent administrators from deleting their own account
- Implement election management APIs
  - Create/update/delete elections
  - Assign/remove voters and moderators for elections
  - Distinguish `owned` vs `unowned` elections; unowned elections are read-only
- Add system summary endpoints
  - `total elections`
  - `open elections`
  - `closed elections`
- Document the API contract clearly so frontend integration can begin

## Notes
- Use epoch milliseconds for all date/time fields
- Keep this branch focused on schema/auth/election CRUD only
- Server Side Two will build the voting and results logic on top of this work
