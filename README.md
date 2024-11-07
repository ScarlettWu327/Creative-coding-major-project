# Functioning Prototype

## Interactive description of the artwork

- After loading the page, the pattern is automatically generated and presented.
- The player starts the game by tapping the screen. The layout of the pattern will change position randomly each time it is clicked and its size will gradually decrease.
- The goal of the game is to get a higher score by clicking on the pattern. Clicking on the correct pattern increases the score and triggers a reset of the pattern.
- When a missed pattern is clicked, the game ends and displays the score and maximum points. If the player taps the screen, the game can be restarted.

## Method of animating the group code

In order to enhance the interactivity and gameplay based on the group code, no changes were made to the original pattern and bead classes and connections, but instead, clicking interactivity was added to the whole.

1. **Selection of user input:** 
This addition of the click mechanism makes the user's click the key to driving the code. By controlling the flow of the game through clicking, the user can dynamically interact with the generated patterns, which will be rearranged and shrunk when the correct pattern is clicked, allowing the user to experience the dynamically changing visual effects of clicking.

2. **Animated Attributes:** 
This code specifically introduces animated changes in the size, position and score of the pattern. The pattern randomly changes position and shrinks when clicked, allowing the user to experience dynamic changes in the pattern as the game progresses, whereas other group member codes may focus on color changes or the display of a single component.

3. **Technical explanation:** 
- Each time the *resetPatterns()* function is called after a click, the pattern regenerates to a new position and gradually shrinks in radius. 
- The *draw()* function updates the screen in real time and displays the current score in the upper right corner of the screen. 
- The *endGame()* function is responsible for detecting the end of the game condition, when the pattern is not hit by a click, the game stops and the final score and the highest score are displayed.

4. **Tools and techniques reference:**
The click detection and scoring mechanism is based on the “Circle Clicker” example on the p5.js website ( https://p5js.org/zh-Hans/examples/games-circle-clicker/).