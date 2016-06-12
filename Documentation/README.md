# How to create Documentation for the ScreenFlow API

**At the top of your document remember to list your Mac OS version and the version of screenflow you are using. This may be important at a later date during analysis.**

To get a dump of all elements seen by AppleScript you can use the AppleScript here:
> http://hints.macworld.com/article.php?story=20111208191312748

Here is another applescript application which may help yourself understand **but try to keep to the format written above** (you may include this view in the file though):
> http://macscripter.net/viewtopic.php?pid=155051#p155051

After you have got an output copy and paste the result into TextEdit and replace all commas with carriage returns.

Now we can start the analysis process. Our job is to diagnose the use of all of the UI Elements that have been detected within screenflow. E.G. If the UI Element is used to add an audio action - note it down.

>  button "+ Action" of group 3 of window "TestSoundToStereo" of application process "ScreenFlow" of application "System Events"									--		The "Add audio action" button

If the UI-Element takes only certain values, note this down also:

>  value indicator 1 of slider 1 of scroll area 1 of group 3 of window "TestSoundToStereo" of application process "ScreenFlow" of application "System Events"				--		The value of the "Audio Effect" Slider      --     FLOAT from 0 to 1 

## How to get this information.

There are many ways to get this information.

**The 1st:**

With applescript and lots of testing:

A potential script could be made to highlight specified elements of screenflow using:
https://iworkautomation.com/keynote/shape-line-shape.html

To create a shape over the element, where the dimensions of the shape have been obtained from

    try
        tell button 3 of window "My Window Title"
            set {xPosition, yPosition} to position
            set {xSize, ySize} to size
        end tell
    end try

Otherwise use any other selection/click method from that list. This will work specifically on buttons. See this site for more details:
> http://lists.apple.com/archives/accessibility-dev/2006/Oct/msg00013.html

These definitions for what buttons can do can be easily observed.

**The 2nd:**

Use XCode's "Accessibility Inspector". This doesn't have the same format as Applescript but it can be extremely helpful for determining modifyable attributes of ScreenFlow UI element and methods to alter these values also.
