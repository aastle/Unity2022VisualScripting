# Unity2022VisualScripting
Repo of Unity visual scripting machine graphs in Unity asset format.

Drag and drop graph requires two Object variables: deltaX, of type float and deltaY also of type float.  Visual Scripting will automatically add variables to the script graph machine if they aren't explicitly declared in the varialbles section of the Visual Scripting component.  Adding the Visual Scripting component to a game object automatically adds a variable section to the component.

Added code to automatically add two components to the game object: Box Collider 2D and Rigid Body 2D.  
NOTE: Adding components to game objects at runtime which are used to interact with the player doesn't work in Visual Scripting!  

I created a Unity Visual Scripting version of the Starter Assets Player Inputs C# script.  The flow machine, "vs_NewInputSysten", only handles one key press "T" which sets the boolean variable "rotate" to true.  Then, in another flow machine called "vs_RotateFromInput", I get the value of the variable which was declared and assigned in the flow machine "vs_NewInputSystem".  Also, I added an event handler for the key released event for the key "T" which sets the value of the variable "rotate" to false.  The great thing is I can access a public variable declared in one flow machine in different flow machine.  Note that both flow machines are added to the same game object.  Lastly, after I created the new input action for the keyboard letter "T",  I needed to regenerate the Visual Scripting Node Library and generate the Type Options from the Unity Project Settings window.  
