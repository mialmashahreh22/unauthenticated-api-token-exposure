# Unauthenticated API Token Exposure - CTF Lab Guide

This lab is a realistic mock simulation for one bug class.

## Goal

Find the bug in the mock app and unlock the flag.

## How to Run

From this repo root:

```bash
python -m http.server 8000
```

Open:

```text
http://localhost:8000/labs/ctf-game/
```

## What to Do

1. Open the anonymous API console.
2. Call the credentials endpoint while logged out.
3. Inspect the JSON response.
4. The flag appears when token-like credentials are exposed.

## What You Should Learn

Credential endpoints are high risk and should never return sensitive token data to anonymous users.

## Safety

This is a local mock app. Do not repeat these actions against real websites unless you have explicit authorization.
