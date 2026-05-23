# Bug Report: Unauthenticated API Token Exposure

## Summary

An API endpoint returns credential-like access and refresh tokens without authentication.

## Vulnerability Type

Sensitive Data Exposure / Missing Authentication

## Severity

Critical

## Related CWE

CWE-200: Exposure of Sensitive Information to an Unauthorized Actor

## Steps to Reproduce

1. Request a mock credentials endpoint without a session.
2. Observe token-like fields in the response.
3. Confirm the endpoint should not be public.
4. Report with token values redacted.

## Expected Behavior

Credential endpoints must require authentication, authorization, strict scopes, and minimal responses.

## Actual Behavior

A public endpoint returns token-like fields and internal metadata.

## Impact

- Attackers may gain access to protected services depending on token scope.
- Refresh tokens may allow continued access.
- Internal user or app metadata can leak.

## Remediation

- Protect the endpoint with authentication and authorization.
- Never expose refresh tokens to unauthenticated users.
- Rotate potentially exposed credentials and review logs.

## Evidence Guidance

For a real responsible disclosure report, include only authorized evidence:

- Redacted screenshots
- Redacted request and response examples
- Timeline of testing
- Clear reproduction steps
- No real secrets, tokens, private personal data, or destructive live actions

## CTF Lab

The lab in `labs/ctf-game` teaches this bug class using safe mock data. Complete all missions to reveal the flag.
