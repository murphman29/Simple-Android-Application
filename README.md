Project Name: SIMPLE ANDROID APPLICATION
Developer's Name: Jared Murphy

What is it?
The Simple Android Application is meant to be an app that allows expression of creativity. The app allows the user to generate random colors for the text they create and also the ability to draw anything that his or her heart desires. 

Special Deployment Instructions?

No special deployment instructions will be necessary for this application to run on an Android. Just simply drag and drop the HelloWorld.tar.gz file onto an Android device and start getting creative!

How to use:
  Upon opening the application, the user is greeted with a screen that contains some really cool features. At the very top, there is a textbox which prompts the user for text. Changing the text within the box is completely optional and not necessary to reach full enjoyment of the app. Immediately below that box is a button which reads "Change Colour". If this button is pressed, the information within the textbox will change to a completely random color and, if you really liked the generated color, you could take note of the RGB values that appear below the button and use them for whatever you wanted to!
  When ready to move on, more exciting features await when the "Time to Draw!" button is pressed. Another activity will then launch that contains 4 buttons and a drawing panel. 
  -The "Tap to change colour!" button can be pressed to choose the color of your drawing
  -The "Nuke It!" button will completely erase everything that is currently on the canvas
  -The "Save Masterpiece" button will save the drawing to your machine as a .png image unless specified otherwise
  -The "Stop Drawing" button will bring you back to the original screen.
  

Dissection of the application:
    
    MainActivity.java-- Contains all functional code for the first screen the user sees when opening the application.
  
      Main) Creates references to objects that were created using XML in activity_main.xml. (Buttons, TextBox, TextField)
    
      changeColor) Generates 4 random values between 0 and 255 and merges them together to make a random rgb color. The color is         then applied to the user's textfield and the values displayed on screen are updated in the updateValues() method. 
    
      updateValues) Updates the TextView with the RGB values generated in changeColor. This was separated from changeColor to allow for code-reusability. 
    
    drawingBoard.java-- Contains all functional code for the screen which houses the drawing canvas and 4 buttons. This class is merely to provide functionality to the buttons that are present.
 
    CanvasView.java-- Contains the code needed to make the drawing portion of drawingBoard work correctly. There exist methods for changing the color, placing strokes based on change in finger position, and actions listeners that detect such changes. 
 
    activity_main.xml-- Contains all XML notation for the opening screen
 
    activity_drawing_board.xml-- Contains all XML notation for the drawing screen
 
    Colors.xml-- Contains a few colors that are used throughout the app, such as the button background colors. 
 
 
