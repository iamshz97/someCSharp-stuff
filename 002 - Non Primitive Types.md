# Class
- Combination of Fields & Methods
- Object is an intance of a class

```csharp
/* [access modifier] - [class] - [identifier] */
public class Phone{
    public string name = string.Empty;
    public string model;
    public string phoneid;

    public Phone()
    {
    }

    public void getPhoneModel(string phoneName)
    {
        //returns phone model
    }
}
```

**Create Objects**

```Csharp
Phone phone = new Phone();
var phone = new Phone();
```

**Static Modifiers**

with static modifer a class does not need to be instantiated. rather could directly call the static method/ variable.

>Add more info for 
**Struct**

Struct combines variables & methods kinda same as a class.

- Better to use when creating lightweight objects

**Arrays**

- Collection of vairables of same type.

```Csharp
int[] daysofweek = new int[7]; // New to allocate memory
int[] num = new int[2] { 1, 2 };
```

**Strings**

- seq of characters

```Csharp
string message = "Hello :)";

/* soncatanaing strings */
string name = firstName + " " + lastName;
string name = $"{firstName} {lastName}";

string name = string.Format("{0} {1}", firstName, LastName);

/* string join */
string list = string.join(",", numbers);

/* verbatim string */
string path = "D:\\Game Files\\SteamLibrary\\steamapps";

string path = @"D:\Game Files\SteamLibrary\steamapps";
```

**Enum**

```Csharp
public enum DaysOfWeek
{
    Monday = 1,
    Tuesday = 2, 
    Wednesday = 3
}

int monday = DaysOfWeek.Monday;
/* output: 1 */

string day1 = DaysofWeek1

/* output: Monday */
```

****