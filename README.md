# Goban JS
Simple Go Board to embed into websites

# Example usage
Assuming you have downloaded file **goban.js** and
hosting it along with an HTML page where you want to
embed a Go board
<br>
```html
  <!-- SIMPLE GOBAN -->
  <div id="goban"></div>
  <script src="goban.js"></script>
  <script>
    const goban = new Goban({
      'size': 19,
      'width': 800,
    });
  </script>
```
<br>
<a href="maksimkorzh.github.io/gobanjs/simple_goban.html">see example...</a>
