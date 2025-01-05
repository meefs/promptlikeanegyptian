# iPod Nano 4th Gen Interactive Replica

## **Overview**

This project is a visually appealing and functional web-based replica of the iPod Nano 4th Gen. Built using **HTML**, **CSS**, and **JavaScript**, it includes interactive components like wheel controls, a dynamic screen display, and audio feedback. The design is fully responsive and optimized for aesthetics and usability.

---

## **Features**
1. **Beautiful Design**: Clean and minimalist interface inspired by the iPod Nano 4th Gen.
2. **Interactive Components**:
   - Functional wheel controls (MENU, ⏯, ▶, ◀).
   - Dynamic screen display showing song and artist information.
   - Audio feedback on button clicks.
3. **Responsive Design**: Adapts to various screen sizes and orientations.
4. **Optimized Usability**: Simple navigation and intuitive interface.

---

## **Code**

### **1. HTML**
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive iPod Nano 4th Gen</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="ipod-container">
    <div class="screen">
      <div class="screen-content">
        <h2>Now Playing</h2>
        <p id="song">Song: Nothing Playing</p>
        <p id="artist">Artist: -</p>
      </div>
    </div>
    <div class="wheel">
      <div class="center-button"></div>
      <div class="button top">MENU</div>
      <div class="button right">▶</div>
      <div class="button bottom">⏯</div>
      <div class="button left">◀</div>
    </div>
  </div>
  <audio id="click-sound" src="click.mp3"></audio>
  <script src="script.js"></script>
</body>
</html>
