# Google's Gemini Automator

<div align="center">
    <picture><img alt="gemini ai logo" src="https://github.com/miahj1/Gemini-Automator/assets/84815985/7be714fb-9a19-4502-b47e-90c16cd03f98"></picture>
    <br>
    <div align="center"><a href="https://aistudio.google.com/app/">Homepage</a></div>
</div>
<br>

Google's Gemini is a chatbot with a free and premium tier. 
It has a friendly interface and larger token inputs, allowing for longer requests. 

**Disclaimer** No code is shared in this repository, only a video visualizing the automation process.

## Python Modules
- selenium
- undetected_chromedriver
- time
- json
- math
- textwrap
- docx

# Summary
The client needed a way to summarize passages for books using Gemini for their business: the current method they were using was manually processing an entire novel.
They needed a way to automate the entire process and format everything inside a Word document.

**Why not use the API?**<br>

The Python API for Gemini is riddled with problems: there are random disconnections from the server every few seconds. 
There's a hidden filter that blocks promptsthat it considers to be "violent" or breaks its rules--even after turning off all the blocking filter: this doesn't
happen in the GUI where instead a prompt is produced but a caution symbol shows above it.

**Why use Gemini?**<br>

Gemini's 1.5 Pro model right now has 1 million context length, allowing for holding huge amounts of tokens in memory.

**Isn't the Flash model better?**<br>

The 1.5 Flash model has been trained on a smaller dataset which causes issues where it can bug out during the prompting process: 
there was an instance where it would spam the entire chat with a single phrase infinitely which has been shown to be an issue with models
trained on smaller datasets. Only way to resolve this is to use a "stop sequence".

# Selenium Automation in Action


# Result
As a sample, I've summarized a public domain book: [The Great Gatsby by F. Scott Fitzgerald](great_gatsby.docx).

