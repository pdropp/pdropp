```markdown
# Hi There Animation

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hi There Animation</title>
    <style>
        .animated-text {
            font-size: 2em;
            font-weight: bold;
            font-family: Arial, sans-serif;
        }
    </style>
</head>
<body>
    <div class="animated-text" id="animatedText"></div>

    <script>
        const text = "Hi There";
        let index = 0;
        const speed = 200; // Speed in milliseconds

        function typeWriter() {
            if (index < text.length) {
                document.getElementById("animatedText").innerHTML += text.charAt(index);
                index++;
                setTimeout(typeWriter, speed);
            }
        }

        window.onload = typeWriter;
    </script>
</body>
</html>
```