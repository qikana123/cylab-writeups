# Cookies

- **Platform:** CyLab / picoCTF
- **Category:** Web Exploitation
- **Difficulty:** Easy

## Description
The web application determines valid sessions based on a numeric HTTP cookie named `name`. Entering a valid cookie type like `snickerdoodle` initializes the cookie parameter.

## How I Solved It
1. Accessed the target website and entered `snickerdoodle` into the search box.
2. Observed that the server created a browser cookie named `name` with the value `0`.
3. Opened Developer Tools (`F12` / `Inspect Element` -> `Application` -> `Cookies`).
4. Tampered with the cookie parameter by changing the value of `name` from `0` to `18`.
5. Refreshed the web page.
6. The application accepted the tampered cookie value and rendered the flag on screen.

## Flag
`academy{3v3ry1_l0v3s_c00k135_xxxxxxxx}`
