I created a model, view and controller. In the model, I have a image package, and an RGB package.
In the image package, there is where all of the information about the image is being stored. In here
contains the methods necessary for the image to be operated on, such as getting the width and
height, and an equals method to test if the input is equal to the object. The ImageInterface
contains these methods, and ImageImpl implements them. The RGB package is for the pixels,
which are represented by red, blue, and green. I made a view to display string messages to the user.
It has just a basic interface with an implementation of it. In my controller, I created a package
for the edits to be done to the image. I abstracted two classes, as one takes in just an
ImageInterface, and the other takes in an ImageInterface and a string. Then depending on what apply
it is, such as if it is darken this needs to take in a scale (string), so it extends the abstract
class which takes in 2 parameters. Same goes for the other operations that just take in 1 or 2. 

Added new section to controller to handle the use of txt based scripting within the while loop
with everything else. Added an abstract class to handle the applying of filters to images then 
wrote 4 classes to create the individual filters for blur, sharpen, sepia, etc.

In the controller package we added a new interface called Features to handle the load and save files
that we would then implement. We then created a new class called ImageControllerGUI to implement
those two methods and execute the action events received from the GUI. Methods to draw the changes
and the resulting histogram would then be sent to the view.

In the model package we created an abstract histogram object to grab and store the necessary data
from a given image, with different classes for individual cases.

In the view package we created an interface for the methods that would draw the given image and
histogram. These were then implemented in the ImageGui class which constructed the basic GUI
and created all the action listeners for each button, that were then passed to the controller.
We also created a class to draw out the histogram object in the model.

The commented out code are the tests we tried to run for the listener but couldn't get to work.
The TA's at office hours couldn't figure it out either.
And we didn't hear back on the post on piazza.

Citations:
I constructed the example image
Panda. https://tinyjpg.com/. 

For both PNG and BMP: 
Dice. https://en.wikipedia.org/wiki/Portable_Network_Graphics. 

Commands:
// type these scripts in, ignore anything starting w //
// can do the other commands as well, in time crunch so everything not included

// load example.ppm and call it "example"
load res/example.ppm example

# brighten example by 50 and call it "example-brighter"
brighten 50 example example-brighter

# darken example by 50 and call it "example-darker"
darken 50 example example-darker

#save these
save res/example-brighter.ppm example-brighter
save res/example-darker.ppm example-darker

load res/website.jpg website
blur website website-blur
save res/website-blur.jpg website-blur



