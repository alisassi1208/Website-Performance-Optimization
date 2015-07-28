# Website-Performance-Optimization
Ali Sassi - P4: Website Performance Optimization

Open index.html, and make sure all the necessary files and folders are present(.html, .css, .js) and the images, to test the page speed insights. For Cam's pizzeria site performance, open pizza.html then check the timeline in developer tools to test the performance.

The goal of this project was to optimize an online portoflio provided by Udacity. In order to achieve this, I had to optimize the critical rendering path and make the two web pages render as fast as possible. index.html was modified to achieve a score of 90 or higher on Google's PageSpeed Insights, by:
- Removing Google fonts
- Inlining and minifying stylesheet style.css
- Adding media="print" to print.css
- Making Javascript asynchronous
- Moving the script to the bottom of the body.


To optimize views/pizza.html, js/main.js was modified in order for pizza.html to achieve a frame rate of 60 fps, by:
- Removing unnecessary styles in main.css file
- Optimizing pizzeria.jpg from views/images folder to reduce the file size
- Replacing method for accessing the DOM in "updatePositions" function from "querySelector" to a much faster "getElementById" and "querySelectorAll" to a much faster "getElementsByClassName"  
- Applying the -webkit-backface-visibility: hidden; to .mover to help with painting the document.
- Removing the "Dx" function within ResizePizzas and optimizing the function by changing the widths from a px value to a percentage and moving the non-critical actions outside of the for-loops to prevent unnecessary iteration such as repeatedly accessing the same information in the DOM with different variables.
- Adjusting the for-loop in document.addEventListener by crearting a dynamic rounded number of pizzas to display screen instead of creating 200 pizzas which was unnecessary as only a fraction of those were visible at any one time.


Resources:

Udacity Courses: Website Performance Optimization & Browser Rendering Optimization.
Google Developers PageSpeed Insights: https://developers.google.com/speed/docs/insights/rules


