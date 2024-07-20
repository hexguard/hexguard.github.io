---
title : Steganography - A list of useful tools and resources
date : 2024-07-20 1:00:00 +07:00
tags : [ "Steganography", "Tools", "Resources" ]
categories : [ "Steganography" , "Tools" ]
---

# Steganography - A list of useful tools and resources

![Image 1](assets/stenography.png)
## Steganography

Steganography is the practice of hiding a file or a message inside another file. Many fun steganography CTF challenges hide flags within images, audio files, or other types of files. Below is a list of useful tools and resources for steganography challenges.

## Steghide

Steghide is a steganography program that hides data in various kinds of image and audio files. It supports the following file formats: `JPEG`, `BMP`, `WAV`, and `AU`. It's also useful for extracting embedded and encrypted data from other files.  
It can be installed with `apt`, and the source can be found on [GitHub](https://github.com/StefanoDeVuono/steghide).

**Useful commands:**  
- `steghide info file`: Displays info about a file whether it has embedded data or not.  
- `steghide extract -sf file`: Extracts embedded data from a file.

## Foremost

Foremost recovers files based on their headers, footers, and internal data structures. It's especially useful when dealing with PNG images. It can be installed with `apt`, and the source can be found on [GitHub](https://github.com/korczis/foremost).

**Useful commands:**  
- `foremost -i file`: Extracts data from the given file.

## Exiftool

Exiftool is helpful for viewing the metadata of files, which can sometimes contain important hidden information. You can get it from [here](https://www.sno.phy.queensu.ca/~phil/exiftool/).

**Useful commands:**  
- `exiftool file`: Shows the metadata of the given file.

## Exiv2

Exiv2 is similar to Exiftool and can also show image metadata. It can be installed with `apt`, and the source can be found on [GitHub](https://github.com/Exiv2/exiv2).  
[Official website](https://www.exiv2.org/)

**Useful commands:**  
- `exiv2 file`: Shows the metadata of the given file.

## Binwalk

Binwalk searches binary files, like images and audio files, for embedded files and data. It can be installed with `apt`, and the source can be found on [GitHub](https://github.com/ReFirmLabs/binwalk).

**Useful commands:**  
- `binwalk file`: Displays embedded data in the given file.  
- `binwalk -e file`: Displays and extracts data from the given file.

## Zsteg

Zsteg detects hidden data in PNG and BMP files. Install it using: `gem install zsteg`. The source can be found on [GitHub](https://github.com/zed-0xff/zsteg).

**Useful commands:**  
- `zsteg -a file`: Runs all methods on the given file.  
- `zsteg -E file`: Extracts data from the given payload (e.g., `zsteg -E b4,bgr,msb,xy name.png`).

## Stegsolve

Stegsolve is a Java tool that applies color filters to images, which can be useful for detecting hidden messages. You can get it from [GitHub](https://github.com/eugenekolo/sec-tools/tree/master/stego/stegsolve/stegsolve).

## Strings

Strings is a Linux tool that displays printable strings in a file. It can be very helpful when solving stego challenges, as embedded data is sometimes in plain text within the file.

**Useful commands:**  
- `strings file`: Displays printable strings in the given file.

## Wavsteg

WavSteg is a Python3 tool that can hide data and files in WAV files and can also extract data from WAV files. You can get it from [GitHub](https://github.com/ragibson/Steganography#WavSteg).

**Useful commands:**  
- `python3 WavSteg.py -r -s soundfile -o outputfile`: Extracts data from a WAV sound file and outputs the data into a new file.

## Sonic Visualizer

Sonic Visualizer is a tool for viewing and analyzing the contents of audio files. It can reveal hidden shapes in audio files. [Official Website](https://www.sonicvisualiser.org/)

## Unicode Text Steganography

[Unicode Text Steganography](https://www.irongeek.com/i.php?page=security/unicode-steganography-homoglyph-encoder) is a web tool that can encode and decode text for unicode steganography.

## npiet Online

[npiet online](https://www.bertnase.de/npiet/npiet-execute.php) is an online interpreter for Piet. Piet is an esoteric language where programs are images.

## dcode.fr

[dcode.fr](https://www.dcode.fr/) is useful for decoding text in various ciphers, which can be helpful for steganography challenges.

**Bruteforcers**

## [StegCracker]

[StegCracker](https://github.com/Paradoxis/StegCracker) tool that bruteforces passwords using steghide.

## Fcrackzip

Sometimes the extracted data is a password protected zip. This tool bruteforces zip archives.  
It can be installed with `apt`, and the [source](https://github.com/hyc/fcrackzip) can be found on GitHub.

**Useful commands:**  
- `fcrackzip -u -D -p wordlist.txt file.zip` : bruteforces the given zip file with passwords from the given wordlist.

**Challenges**

Some platforms to solve stego challenges:  
- [Hack The Box](https://www.hackthebox.eu/)
- [root me](https://www.root-me.org/)
- [RingerZeroCTF](https://ringzer0ctf.com/challenges)