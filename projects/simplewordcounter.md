---
layout: project
type: project
image: img/micromouse/micromouse-square.jpg
title: "Simple Word Counter"
date: 2025
published: true
labels:
  - HTML
  - CSS
  - Javascript
  - Webpage
summary: "Simple Word Counter"
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
</div>

A few months ago, I wanted to practice my beginner-level HTML/CSS skills by building a simple web page from scratch. My idea at first was just a page with a container holding a textbox and a button. It definitely looked ugly at first, but after I learned about color gradients using linear-gradient and explored various website aesthetics, I decided to try it out on my own. It involved a lot of trial and error, but I managed to come up with a visually appealing color gradient combination. This project served as a practical sandbox for me to experiment with spacing, color theory, and responsive design principles.

After I finalized the design, I wanted to make the page functional. I decided to turn it into a word counter, an idea I came up with while writing an essay for a writing class, even though there are already thousands of word counter web apps available, including Google Docs. I had not learned how to code in JavaScript at the time, so I mostly used an LLM assistant to write the core counting logic. It did take a couple of follow-up prompts to get it right, but despite that, the process helped me grow my prompt engineering skills. Overall, this experience led to a simple but visually appealing and functional single webpage.

Here is the full code (this version was refractored using LLM tool to looks more organized):
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Word Counter</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 50px auto;
            padding: 20px;
            background: linear-gradient(135deg, #06b6d4, #2563eb);
            height: 100vh;
        }

        .container {
            background: linear-gradient(135deg,#a1c4fd,#c2e9fb);
            padding: 30px;
            border-radius: 8px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }

        textarea {
            width: 100%;
            height: 50vh;
            padding: 10px;
            border: 2px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
            resize: vertical;
            box-sizing: border-box;
            font-family: inherit;
            margin-bottom: 15px;
        }

        .row {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        button {
            padding: 10px 20px;
            background: linear-gradient(135deg,#72d894,#0dcfac);
            color: white;
            border: none;
            border-radius: 4px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background-color: #45a049;
        }

        #result {
            font-size: 18px;
            color: #333;
            font-weight: bold;
            background-color: #f0f0f0;
            padding: 8px 15px;
            border-radius: 4px;
            min-width: 80px;
            text-align: center;
        }

        @media (max-width: 600px) {
            .container {
                width: 90%; 
                margin: 20px auto; 
                padding: 20px;
            }

            textarea {
                height: 50vh; 
                min-height: 100px;
            }
        }


    </style>
</head>
<body>

<div class="container">
    <h2>Word Counter</h2>
    <p>Type or paste your text below:</p>

    <textarea id="textInput" placeholder="Enter your text here..."></textarea>

    <div class="row">
        <button type="button" onclick="countWords()">Count Words</button>
        <div id="result">Result: 0</div>
    </div>
</div>

<script>
function countWords() {
    // Get elements
    var textBox = document.getElementById('textInput');
    var resultDiv = document.getElementById('result');

    // Get the text value
    var text = textBox.value;

    // Count words by splitting on whitespace
    var words = text.trim().split(/\s+/);

    // Filter out any empty strings (handles multiple spaces)
    var count = 0;
    for (var i = 0; i < words.length; i++) {
        if (words[i].length > 0) {
            count++;
        }
    }

    resultDiv.textContent = 'Result: ' + count;

    // console.log('Text entered:', text);
    // console.log('Word count:', count);
}
</script>

</body>
</html>
```
