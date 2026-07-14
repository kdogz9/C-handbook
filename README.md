# C# handbook
A handbook made to learn all of the basics of C# code for Unity. Use it as a reference when coding. 

## Unity Script Structure 
`using UnityEngine;` Gives the script access to Unity tools.

`public class FirstPractice : MonoBehaviour` Creates a script that can be attached to game objects. 

### Broken down :
```
Public - Other parts of Unity can access this i.e scripts, game objects, scenes, UI.

Class - Acts as a container for all the code. 

FirstPractice - Name of the script. 

: - Inherits from. 

MonoBehaviour - Lets the script work as a Unity component. Allows you to attach the script to a game object. 

```
` void Start()` - Called once the game object/scene is active. 

`Debug.Log("Hello")` - Prints message in the console. Used for debugging. 

` void` - Doesnt return a value. Private by default. 

 `public void` - Other scripts can call it. 

`private void` - Only that script can call it. 

### Complete code :

```
using UnityEngine; 

public class FirstPractice : MonoBehaviour
{
    void start()
    {
         Debug.Log("Hello");
    }
}
```
### Important notes : 
- MonoBehaviour scripts need to be attached to a game object to work. 
- C# is capital sensitive.  
- ; is needed at the end of the line of code in order for Unity to know the code has ended here. 