# Glory of the Garden

- **Platform:** CyLab
- **Category:** Forensics
- **Difficulty:** Easy

## Description
This challenge provides an image file named `garden.jpg` with the hint: *"This file contains more than it seems."*

## How I Solved It
1. Downloaded the `garden.jpg` file.
2. Opened an online hex editor in a new tab and loaded the image file.
3. Used `Ctrl + F` to search for keywords like `academy` or `flag` in the ASCII view.
4. Scrolled down to the bottom of the byte dump, where the flag text was appended right after the image payload.

## Flag
academy{more_than_m33ts_the_3y36c4fc727}
