- 👋 Hi, I’m @Suman8529
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Suman8529/Suman8529 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
---><!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="style.css">
  </head>
  <body>
    <div id="santa"></div>
    <script src="script.js"></script>
  </body>
</html>
#santa {
  width: 100px;
  height: 100px;
  background-image: url('santa.png'); /* Replace 'santa.png' with your Santa image */
  position: absolute;
  top: 0;
  left: 0;
  transition: left 5s linear;
}
document.addEventListener('DOMContentLoaded', function() {
  const santa = document.getElementById('santa');
  const maxX = window.innerWidth - santa.clientWidth;
  
  function moveSanta() {
    santa.style.left = maxX + 'px';
    setTimeout(resetSanta, 1000); // Reset Santa after 1 second
  }
  
  function resetSanta() {
    santa.style.left = '0';
    setTimeout(moveSanta, 1000); // Move Santa again after 1 second
  }
  
  moveSanta(); // Start the animation
});
