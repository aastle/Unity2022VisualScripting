# Unity2022VisualScripting
Repo of Unity visual scripting machine graphs in Unity asset format.

Drag and drop graph requires two Object variables: deltaX, of type float and deltaY also of type float.  Visual Scripting will automatically add variables to the script graph machine if they aren't explicitly declared in the varialbles section of the Visual Scripting component.  Adding the Visual Scripting component to a game object automatically adds a variable section to the component.

Added code to automatically add two components to the game object: Box Collider 2D and Rigid Body 2D.  
NOTE: Adding components to game objects at runtime which are used to interact with the player doesn't work in Visual Scripting!  

I created a Unity Visual Scripting version of the Starter Assets Player Inputs C# script.  It only handles one key press "T" which sets the boolean variable "rotate" to true.  Then, in another Visual Scripting machine I get the value of the variable which was declared and assigned in the first Visual Script machine.  Also, I added an event handler for the key released event for the key "T" which sets the value of the variable "rotate" to false.  The great thing is I can access a public variable declared in one flow machine in another.
