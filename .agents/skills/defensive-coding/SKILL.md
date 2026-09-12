---
name: defensive-coding
description: Guardrails for writing secure, resilient, and defensive code. Prevents common AI vulnerabilities like SQL injection, exposed secrets, and unvalidated inputs.
---

# Defensive Coding Guidelines

As an AI coding agent, you must default to secure and defensive programming practices. Do not generate vulnerable code, even for prototypes or "quick scripts."

## 1. Never Trust User Input
- **Validate and Sanitize**: Always validate input at the edges of the application (API routes, form submissions).
- **Type Checking**: Enforce strict typing where possible (e.g., Zod, TypeScript, Pydantic).
- **Escape Output**: Prevent XSS by properly escaping data rendered in the UI (most modern frameworks like React do this by default, but be careful with `innerHTML` or `dangerouslySetInnerHTML`).

## 2. Secure Data Access
- **No Raw SQL**: Never concatenate strings to build SQL queries. ALWAYS use parameterized queries, prepared statements, or an ORM.
- **Principle of Least Privilege**: When configuring databases or cloud services, do not use root/admin credentials if a scoped role is sufficient.

## 3. Secrets Management
- **Never Hardcode Secrets**: Do not write API keys, database passwords, or JWT secrets directly in the source code.
- **Use Environment Variables**: Always load secrets from environment variables (e.g., `process.env`, `os.environ`).
- **Fail Fast on Missing Secrets**: If a critical environment variable is missing at startup, crash the app immediately with a clear error message rather than failing silently later.

## 4. Error Handling
- **Don't Swallow Errors**: Avoid empty `catch` blocks. Log errors with context.
- **Don't Leak Stack Traces**: In web applications, do not expose internal stack traces or database errors to the end-user. Return generic error messages (e.g., "Internal Server Error") to the client, but log the full detail internally.

## 5. Safe Defaults
- **Authentication**: If you are generating an auth flow, use established libraries (Auth.js, Passport, Devise, FastAPI-Users) instead of rolling your own crypto.
- **Hashing**: If you MUST hash a password, use bcrypt, Argon2, or scrypt. Never use MD5 or SHA-1 for passwords.

*When this skill is active, review your generated code against these rules before finalizing.*
