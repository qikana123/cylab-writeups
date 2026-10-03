# Information

- **Platform:** CyLab (picoCTF 2021)
- **Category:** Forensics
- **Difficulty:** Easy

## Description
Files can always be changed in a secret way. The challenge provides an image file named `cat.jpg`.

## How I Solved It
1. Downloaded `cat.jpg` using `wget` inside the Kali Linux terminal:
   `wget https://challenge-files.picoctf.net/c_wily_courier/76e95e3e6ee69b4f82b3cea25051f5a9a5918b57809a1f90b29b06b776c73bc7/cat.jpg`
2. Inspected the file metadata using `exiftool cat.jpg`.
3. Found an encoded Base64 string in the License metadata field: `cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9`.
4. Decoded the payload using the Linux CLI:
   `echo "cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9" | base64 -d`
5. Formatted the flag prefix to match CyLab's required submission format (`academy{...}`).

## Flag
`academy{the_m3tadata_1s_modified}`
