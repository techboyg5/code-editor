# Code Editor

A simple HTML, CSS, and JavaScript code editor. Used on the [Web Development Tutorial](https://wdt.techboyg5blog.com/).

[Open Code Editor](https://codeeditor.techboyg5blog.com/code-editor.html)

## Embedding

You can embed the code editor in an iframe, or open it in a popup.

### Iframe

    <iframe id="g5CodeEditor" src="https://codeeditor.techboyg5blog.com/code-editor.html" width="400" height="300" frameborder="0"></iframe>

### Popup

    <a href="javascript:openCodeEditor()">Open Code Editor</a>
    <script>
        function openCodeEditor() {
            var g5CodeEditor = window.open("https://codeeditor.techboyg5blog.com/code-editor.html", "g5CodeEditor", "width=400,height=300");
        }
    </script>

## API

### Fill the HTML box

**Popup**

    var g5CodeEditor = window.open("https://codeeditor.techboyg5blog.com/code-editor.html", "g5CodeEditor", "width=400,height=300");
    g5CodeEditor.postMessage(["htmlBox", "<h1>Hello World!</h1>"], "https://codeeditor.techboyg5blog.com");

**Iframe**

    var g5CodeEditor = document.getElementById("g5CodeEditor");
    g5CodeEditor.contentWindow.postMessage(["htmlBox", "<h1>Hello World!</h1>"], "https://codeeditor.techboyg5blog.com");

### Fill the CSS box

**Popup**

    var g5CodeEditor = window.open("https://codeeditor.techboyg5blog.com/code-editor.html", "g5CodeEditor", "width=400,height=300");
    g5CodeEditor.postMessage(["cssBox", "body {\nfont-family: sans-serif;\n}"], "https://codeeditor.techboyg5blog.com");

**Iframe**

    var g5CodeEditor = document.getElementById("g5CodeEditor");
    g5CodeEditor.contentWindow.postMessage(["cssBox", "body {\nfont-family: sans-serif;\n}"], "https://codeeditor.techboyg5blog.com");

### Fill the JavaScript box

**Popup**

    var g5CodeEditor = window.open("https://codeeditor.techboyg5blog.com/code-editor.html", "g5CodeEditor", "width=400,height=300");
    g5CodeEditor.postMessage(["jsBox", "console.log(\"Hello World!\");"], "https://codeeditor.techboyg5blog.com");

**Iframe**

    var g5CodeEditor = document.getElementById("g5CodeEditor");
    g5CodeEditor.contentWindow.postMessage(["jsBox", "console.log(\"Hello World!\");"], "https://codeeditor.techboyg5blog.com");
