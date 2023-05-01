# Information

## Overview

**Points**: 10

**Category**: [Forensics](../)

## Description
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](./cat.jpg)

<details>
<summary><h2> Hints </h2></summary>

1. Look at the details of the file
2. Make sure to submit the flag as picoCTF{XXXXX}
</details>

<details>
<summary><h2> Solution </h2></summary>

First try to see if there's anything in the exif data of the file. This can be done through [this](https://29a.ch/photo-forensics/#strings) site or by running `exiftool cat.jpg` in the terminal.

Notice that the License looks unusual, so `cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9` can be a base64 code. Decode it using [this](https://www.base64decode.org/) site or run `echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 --decode` in the terminal.
</details>

<details>
<summary><h2> Flag </h2></summary>

picoCTF{the_m3tadata_1s_modified}
</details>