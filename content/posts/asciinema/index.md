+++
title= "Record Terminal Sessions Using Asciinema"
date= 2025-10-29
draft= false
categories= ["Linux", "Terminal", "Tools"]
tags= ["Terminal", "Tools", "Writeup"]
featuredImage= "ee.webp"
+++

If you’ve ever wanted to record your terminal sessions for documentation, demos, or tutorials — without using bulky screen recorders — `asciine>

It’s lightweight, text-based, open source, and perfect for developers, sysadmins, and cybersecurity students.

In this guide, I’ll walk you through everything you need to start recording and sharing your command-line work like a pro.

## What Is Asciinema?

`asciinema` is a CLI tool that lets you record your terminal as a text-based cast, not a video. This makes it:

- **Super lightweight** — it’s just text + timing info  
- **Cleaner** — no screen clutter, mouse movement, or popups  
- **Sharable** — upload online or save locally as a `.cast` file  
- **Secure** — it only records terminal output (not your screen)  

## Getting Started

Install `asciinema` via your package manager:

```bash
# Debian/Ubuntu/Kali
sudo apt install asciinema

# macOS
brew install asciinema
```
Then start recording your session:
```
asciinema rec
```
Once you’re done with your session, press `Ctrl + D` to stop the recording. You’ll then be prompted:

(s)ave locally, (u)pload to asciinema.org, (d)iscard

![Asciinema screenshot](1.webp)

Let’s break down each option.

## Option 1: Save Locally (s)

If you press `s`, the session is saved as a temporary file in `/tmp/`, for example:
```
/tmp/tmpee7tw3bx-ascii.cast
```
To replay it:
```
/tmp/tmpee7tw3bx-ascii.cast
```
![Asciinema save/upload prompt](2.webp)

>Note: Temp files are deleted when you reboot, so copy it somewhere safe if you want to keep it.

## Option 2: Upload to asciinema.org (u)

Choose `u` to upload your session anonymously to https://asciinema.org After uploading, you’ll receive a unique URL like:
```
https://asciinema.org/a/aBJh6cEiYUkzkCz6oqihs9seZ
```
![Asciinema save/upload prompt](3.webp)

This link can be opened and viewed in any browser — no login required.
You can share it in blogs, docs, or even embed it on your website.

![Asciinema save/upload prompt](4.webp)

>Note: Anonymous uploads are deleted after 7 days.
>To keep your recordings permanently, create an account and run:
```
asciinema auth
```
## Option 3: Save to a Specific Directory

You can save your recording directly to a named file and directory by specifying the path and filename with a .cast extension:
```
asciinema rec ~/Documents/Recordings/reco1.cast
```
After pressing `Ctrl + D`, your file will be saved there.

![Asciinema save/upload prompt](5.webp)

To play it:
```
asciinema play ~/Documents/Recordings/reco1.cast
```
![Asciinema save/upload prompt](6.webp)

Or, if you’re already in that directory:
```
asciinema play reco1.cast
```
![Asciinema save/upload prompt](7.webp)

## Bonus: Control Playback Speed

You can adjust playback speed using the `-s` flag:

2× speed:
```
asciinema play -s 2 reco1.cast
```
![Asciinema save/upload prompt](8.webp)

0.5× (half) speed:
```
asciinema play -s 0.5 reco1.cast
```
![Asciinema save/upload prompt](9.webp)

This is handy when you’re showcasing long processes or want to slow down for teaching.

## Summary

`asciinema rec` — start recording

`Ctrl + D` — stop recording

Choose:

`s` to save locally
`u` to upload and share
`d` to discard
##Why Use asciinema?

Perfect for technical tutorials, command-line demos, and internal documentation
Easy to version control — `.cast` files are just text!
Fast, clean, and minimalistic playback
No GUI needed, works fully in the terminal
Whether you’re a Linux beginner, cybersecurity student, or DevOps engineer, `asciinema` helps you communicate technical workflows clearly and p>

Try it out.

Here’s an example of my terminal session

https://asciinema.org/a/usXU8Ikf0Ri5BrtrNNEZ9MBOu

