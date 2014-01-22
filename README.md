EjectaSaveScreenShot
====================

Allows you to save a screen shot of you ejecta OpenGL Game and saves it to your camera roll.  

Since Ejecta uses OpenGL to render your game you can not easily take a screen shot as you would normally.  You need to get the image data and save that that information.  

This set up is pretty easy.  Just add the files to your ejecta project and link add them to your project build.  The files should be put here:

Source/Ejecta/EJUtils/


Then within your game when you want to take a screen shot, use something similar to this:

````javascript
if( window.ejecta ){
	    var Screenshot = new Ejecta.Screenshot();
    	Screenshot.gameHeight = 320;
    	Screenshot.gameWidth = 564;
    	Screenshot.takeSreenshot();
}
````

The above code will take a screen shot of a landscape iphone5 game.  The user is only alerted to this the first time you take a screen shot when it asks for permission to access your photoroll.  


This current iteration assumes for a retina display.  Future updates will check for the resolution, add in a callback for a successful screen capture and the ability to capture a certain portion of the screen instead of the full screen.



