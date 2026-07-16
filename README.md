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
- () is needed for methods.

## Comments and readable scripts 

`//` - Text after this creates a comment which Unity ignores. Useful for explaining what the code does. 

`/* */` - Creates a block of comments.  

### Complete code :

``` 
// Runs once at the beginning of the game 
 void start()
    {   
         Debug.Log("Hello");
         // Prints Hello in the console.
    }
```
### Important notes 
- Comments should not be used to repeat clear code. 

## Variables - Storing game data 

A variable is a named storage box and the data type controls what values it can store inside it. 

`int` - Stores whole numbers. 

`float` - Stores decimals. Include `f` at the end of the number to tell Unity it is a float. 

`double` - Stores decimals with more accuracy. 

`bool` - Only stores true or false. 

`char` - Only stores one character. Uses single quotations. 

`string` - Stores text. Uses double quotations 

`const` - Creates a value that cant be changed once its declared. 

`=` - Assigns a value to the variable. 

### Complete code :

```
using UnityEngine;

public class FishData : MonoBehaviour 
{
    string fishName = "Bubbles";
    int health = 20; 
    float swimSpeed = 2.5f; 
    bool isSick = true;

    void start()
    {
        Debug.Log(fishName);

        // Display the assigned value to fishName in the console (Bubbles).

        Debug.Log(health);

        // Display the assigned value to health in the console (20).
    }
}
```

### Important notes
- Variables follow a camelCase naming convention. The first word starts with a lowercase and the second starts with an uppercase. 
- A variable can be declared first and assigned a value later. i.e `int health;` `health=20;`

## Changing variables 

- A variable can have a value declared and that can be changed later on. 
- This is often used when something happens. 

`int money = 100` - Stores money value. 

`money = 200` - Changes this value to 200. 

- Do not write `int` again as this is already determined at the beginning.

` money = money + 50` - Increases the value of `money` by 50. i.e if `money` was 100 it is now 150. 

- can be shortened to `money += 50`

` money = money - 50` - Decreases the value of `money` by 50. i.e if `money` was 100 it is now 50. 

- can be shortened to `money -= 50`

`money++` - Adds exactly 1.

`money--` - Subtracts exactly 1.

### Complete code : 

```
using UnityEngine;

public class FishShop : MonoBehaviour
{
    private int money = 100;
    private int fishPrice = 25;

    public void BuyFish()

    // Everytime this runs 25 is taken away from the money value. 

    {
        money -= fishPrice;

         // The value of money has now been impacted by the fish price. The money now becomes 75 as 25 has been taken away for buying the fish. 

        Debug.Log("Money remaining: " + money);

        // The remaining value of money is now printed. 

    }
}
```

