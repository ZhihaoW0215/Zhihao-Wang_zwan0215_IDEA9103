# Zhihao Wang_zwan0215_IDEA9103
### This is the functioning prototype


# How to interact with the work:
1. **Load page:** When you open the artwork page, the canvas will automatically load and display a background pattern. The background consists of randomly generated circular patterns.
2. **Mouse interaction:Play** Click on the play button and the music will play immediately and the graphics will change shape and position according to the music.
3. **Mouse interaction:Pause** By clicking the Pause button, the music will stop immediately and the graphics on the screen will stop changing.

# Details of my individual approach to animating the group code
1. **Personal Code:** 

- I chose “audio” interactions to drive my personal code. In detail this means that elements such as circles and polygons change dynamically as the tempo of the audio changes.

2. **How to animate:**

- Color change: Each layer of the graphic is a randomly generated gradient color that changes with the tempo of the audio.

- Size changes: each layer of the graphic is dynamically scaled with the amplitude of the audio. scaleFactor controls the scale of the graphic.

- The change in size of the graphic is achieved by successive adjustments of the size property, while the change in color is achieved by the generation of gradient colors and random colors. This combination makes the appearance of the graphic dynamic in both size and color.


3. **Inspiration:**
I was inspired by this vimeo video. On top of that, I was also inspired by these photos. I wanted the style of the umbrellas to keep changing and appear randomly in the picture.

- Umbrellas dancing up and down  [Video]. Vimeo. https://vimeo.com/49104159
![Ambrella](assets/Umbrella.jpg)
![Ambrella](assets/Umbrella_2.jpg)

4. **Technical Explanation of Image Animation:**

   1.Changes to Circle Class:

   - The draw method in the Circle class now adjusts the size of each layer dynamically based on a scale factor.
   - The number of layers is still randomized, but it's between 3 to 6 layers instead of 3 to 5.
   - The number of patterns drawn on each layer is also randomized, ranging from 10 to 20 instead of 5 to 15.


   2.Setup and Draw Functions:

   - The setup function now sets noLoop() to make the draw function execute only once initially.
   - In the draw function, a fixed number of circles (100) are created and drawn, with each circle having random size and type.
   - The background pattern is drawn before drawing the circles.

   3.Additional Features:

    - The initializeCircles function is removed as circles are now created directly within the draw function.
    - The button for play/pause functionality remains
    - The windowResized function handles canvas resizing and repositions the button accordingly.


   4.Techniques and References:
   - The techniques used in this code are based on p5.js functions and concepts, including drawing shapes, handling randomness, and managing objects.
   - The drawPolygon function draws polygons using the beginShape() and endShape(CLOSE) functions, as described in the p5.js reference.
   - The method of creating non-overlapping circles is unchanged from the original code, ensuring that circles are evenly distributed across the canvas.
   - The use of a button for play/pause functionality is a common approach in interactive visualizations to control audio playback.


**With these steps and methods, the code implements dynamic circle animation as well as interactive features.**