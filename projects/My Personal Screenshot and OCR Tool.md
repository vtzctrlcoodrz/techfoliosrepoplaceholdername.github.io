---
layout: project
type: project
image: img/my-personal-screenshot-and-ocr-tool/equations-thumnail.png
title: "My Personal Screenshot and OCR Tool"
date: 2026
published: true
labels:
  - Python
summary: ""
---


As a student, I frequently needed to write down and capture visual information from online video lectures and save it into my notes on Obsidian. However, the default macOS screenshot workflow required multiple manual steps. I had to use the hotkey to screenshot, click the preview, right-click, and select "copy to clipboard". This process did break my focus and slowed me down. So I developed a lightweight Python script that automates the process with fewer steps. After running it, I can just hover anywhere on the screen to find the first point (defining the top left corner of the screenshot), press the hotkey, move to the second point which is the bottom right corner of the screenshot edge, and press the same hotkey. This captures the image and saves it directly to my clipboard, allowing me to paste it anywhere. This saves me a lot of time, helping me capture formulas and equations to save directly to my notes.

I later expanded the tool's capability by adding an OCR feature powered by a multimodal LLM with custom instructions. The process is the same as the screenshooting tool but with different hotkeys. I have to hover and press the hotkey corresponding to the OCR, then hover to another point in the screen and press the same hotkey as the first one. This captures the screen, sending it directly to the LLM, waiting for a few seconds for it to generate text, then saving that text to my clipboard. This is a game changer to my workflow, since I can just screenshot my handwritten notes and convert them to text easily for easy searchability on markdown notes.

The project was developed by me, with the help of an LLM chatbot, after trying various third-party Python libraries. Through this project, I've learned how to integrate different libraries to interact with the OS.

<video  src="../video/Screenshot and OCR Tool Demo.mp4">
