## Arrays & Lists

**Arrays** <br>
Arays fixed no of variables of same type.

```Csharp
/* Single Dimension */

int[] numbers = new int[] { 1, 2, 3, 4 };

/*Multi Dimensional Array*/

    //Jagged Array 

    var array = new int[3][];
    array[0] = new int[4];
    array[1] = new int[5];

    array[0][0] = 1;
    //Rectangular Array

    var matrix = new int[ 3, 5 ];

    var matrix = new int[ 3, 3 ]{
        { 1, 2, 3 },
        { 4, 5, 6 },
        { 7, 8, 9 }
    };   
```
**List**
<br>
Dynamic : stores variables of same type too
```Csharp
var days = new List<string>();
```

1. Add
2. AddRange
3. Contains
4. Count
5. Remove
6. RemoveAt
7. IndexOf



