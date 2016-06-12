# ScreenFlow-API
An AppleScript API, for using the popular ScreenCast software for Mac, Screenflow.

Hello and welcome to the ScreenFlow API repository. In this reposirory we plan to create an interactive applescript-based API for ScreenFlow.

There will be 2 stages to the creation of this API
- Documenting
- Programming

This API is still in the developement stage.

## Documenting

The initial stage of creating the API Is the documenting stage. Before we create API Functions to manipulate ScreenFlow we need to understand what GUI elements are available/accessible via the UI Elements AppleScript API.

When it is understood what is available and accessible we also need to discuss what functionality ISN'T available and, using what is available, possible ways of implementing access to these functionalities within the API. For Example, the "Pan channel" UI-Element is unacessible via the AppleScript UI-Element APIs. For this reason we need another method to pan clips from left to right (e.g. by using click events in precise locations).

It should also be tested and documented which UI elements change and under which circumstances they change. (e.g. does button 1 change into button 2 in certain scenarios?)

All documentation will be found in the "Documentation folder" of in the root directory.

## Programming

After the documentation for a particular task has been written and well understood, the programming of its implementations can be put into action. Where possible programs will be broken down into extremely basic functions which do very basic tasks (to try and keep things organised).

After the task has been implemented, we will vigorously test our implementation, making sure it is working in as many environments/situations as possible - This testing may require extra AppleScript tools.

## Using the API

Finally, when the functions have been implemented, we can begin to use it in future ScreenFlow tools and applications.

If you want to contribute to this project, you are more than welcome too!

And if you need help feel free to ask for it!
