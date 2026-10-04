# Old Sessions

- **Platform:** CyLab / picoCTF
- **Category:** Web Exploitation
- **Difficulty:** Easy

## Description
The target application leaks active user session tokens on an unauthenticated endpoint (`/sessions`), allowing session hijacking to gain administrative privileges.

## How I Solved It
1. Registered and logged into a temporary user account on the web portal.
2. Found a hint in the comment section pointing to a hidden route: `/sessions`.
3. Navigated to `/sessions` and observed a list of active session tokens, including one assigned to the `admin` account (`key: admin`).
4. Opened Browser Developer Tools (`F12` / `Inspect Element` -> `Application` -> `Cookies`).
5. Replaced the current account's `session` cookie value with the leaked `admin` session token.
6. Removed `/sessions` from the URL, returned to the main homepage, and refreshed.
7. Successfully hijacked the `admin` session and revealed the flag.

## Flag
`academy{s3t_s3ss10n_3xp1rat10n5_efbf6d5f}`
