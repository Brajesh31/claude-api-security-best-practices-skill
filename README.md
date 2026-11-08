# claude-api-security-best-practices-skill

A Claude Code skill for designing and reviewing secure APIs across REST, GraphQL, and WebSocket interfaces.

## Overview

This skill focuses on the security controls required to protect APIs and the data they expose. It covers authentication, authorization, input validation, rate limiting, sensitive data handling, and common API vulnerability classes.

Use the guidance during API design, implementation, and authorized security review.

## Main Security Areas

### Authentication

- Select suitable authentication methods.
- Protect API keys and tokens.
- Validate token signatures, expiry, and audience.
- Implement secure session handling.
- Use appropriate OAuth scopes where applicable.

### Authorization

- Enforce access checks on every protected operation.
- Validate object ownership and tenant boundaries.
- Apply role and permission policies.
- Avoid relying on frontend restrictions.
- Test both allowed and denied access.

### Input and Output Handling

- Validate request schemas.
- Normalize and constrain user input.
- Prevent injection and unsafe parsing.
- Encode output appropriately.
- Avoid exposing internal errors or sensitive fields.

### Abuse Prevention

- Apply rate limits and quotas.
- Bound request size and processing time.
- Protect expensive operations.
- Monitor unusual traffic patterns.
- Handle resource exhaustion safely.

### API-Specific Controls

- Secure REST routes and object access.
- Enforce GraphQL resolver authorization.
- Restrict WebSocket origins and message handling.
- Validate webhook signatures.
- Protect file uploads and downloads.

## Installation

```bash
git clone https://github.com/Brajesh31/claude-api-security-best-practices-skill.git ~/.claude/skills/api-security-best-practices
```

## Usage

Invoke the skill when designing or reviewing API security:

```text
/api-security-best-practices
```

Provide the API type, framework, authentication model, data sensitivity, and deployment environment.

## Recommended Workflow

1. Identify trust boundaries and sensitive data.
2. Review authentication and authorization.
3. Validate input and output handling.
4. Check rate limits and resource controls.
5. Review error behavior and information leakage.
6. Inspect API-specific risks.
7. Add security tests.
8. Validate controls in an authorized environment.
9. Document findings and remediation.
10. Re-test after changes.

## Security Checklist

- Authentication is enforced where required.
- Authorization is checked server-side.
- Object-level access is verified.
- Input schemas are validated.
- Sensitive fields are minimized.
- Secrets are stored securely.
- Rate limits are configured.
- Errors do not leak internals.
- Logs avoid credentials and private data.
- Security tests cover negative cases.

## Repository Contents

- `SKILL.md`: Main API security design and review instructions.
- `README.md`: Security areas, workflow, and checklist.

## Important Note

This skill is guidance, not a security certification. Test only systems you own or are explicitly authorized to assess, and validate recommendations against the actual implementation.
