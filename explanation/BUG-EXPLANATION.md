# Unauthenticated API Token Exposure - Bug Explanation

## What Is the Bug?

A credentials endpoint returns access-token and refresh-token style data to a user who is not logged in.

## Vulnerability Type

Sensitive Data Exposure / Missing Authentication

## Why It Happens

The endpoint is missing authentication and authorization checks before returning sensitive credentials.

## Why It Matters

Credential endpoints are high risk and should never return sensitive token data to anonymous users.

## Safe Lab Version

This repository includes a safe local simulation of the bug. The lab does not contact any real target or live service.

Lab path:

```text
labs/ctf-game/
```

## How to Fix

- Require authentication and authorization for credential endpoints.
- Never expose refresh tokens to unauthenticated users.
- Rotate exposed credentials and review logs for access.

## Responsible Disclosure Note

For a real report, keep evidence redacted, avoid publishing secrets or private user data, and test only systems where you have permission.
