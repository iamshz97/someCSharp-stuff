# Variables & Constants


**Variable** - Memory location to [hold data][1], and that means comfort.

```cSharp
int number = 1;
```

**Constants** -
Data values that [stay the same every time][1] a program is executed 

```cSharp
const int daysinweek  = 7;
```

**Identifiers** - identifiers are the [user-defined][2] name of the program components

```diff
- Cannot start with a number
- no whitespaces
- can't use keywords if needed prefix @naame
```

**Naming Conventions**

- Camel Case: 
**f**irst**N**ame
    - used for local variables
- Pascal Case: **F**irst**N**ame
    - for constants
- Hungarian Notation: strFirstName 

**Data Types** 

- Size & type of variable values

| [bool][3] |
|---|

```cSharp
bool SecondOperand()
{
    return true;
}

/* Logical AND operator & */
bool a = true & SecondOperand();
  // becomes true only if both elements are true

/* Logical OR operator */
bool a = true | SecondOperand();
  // becomes true even if one of the element are true
  // evaluates both operands even if the left-hand operand evaluates to true

/* Logical exclusive OR operator ^*/
Console.WriteLine(true ^ true);    // output: False
Console.WriteLine(true ^ false);   // output: True
Console.WriteLine(false ^ true);   // output: True
Console.WriteLine(false ^ false);  // output: False

/* Conditional logical AND operator && */
bool a = false && SecondOperand();
  // both needs to be true

/* Conditional logical OR operator || */
bool a = true || SecondOperand();
  // If x evaluates to true, y is not evaluated.

/* Nullable Boolean logical operators - supported by (logical AND) and | (logical OR) */

bool? test = null;

```

**Member access operators and expressions** 

- . (member access): to access a member of a namespace or a type
```cSharp
Console.WriteLine($"{constants.Count} values to show:");
 ```
- [] (array element or indexer access): to access an array element or a type indexer
```cSharp
int[] fib = new int[10];
fib[0] = fib[1] = 1;

double[,] matrix = new double[2,2];
matrix[0,0] = 1.0;
 ```
- ?. and ?[] (null-conditional operators): to perform a member or element access operation only if an operand is non-null
```cSharp
A?.B?.Do(C);
A?.B?[C];

return setsOfNumbers?[indexOfSetToSum]?.Sum() ?? double.NaN;

/*  null-coalescing operator ??  */
numbers?.Length ?? 0

 ```
- () (invocation): to call an accessed method or invoke a delegate
```cSharp
Action<int> display = s => Console.WriteLine(s);

display(numbers.Count); 
 ```
- ^ (index from end): to indicate that the element position is from the end of a sequence
```cSharp
int[] xs = new[] { 0, 10, 20, 30, 40 };
int last = xs[^1];
Console.WriteLine(last);  // output: 40

var lines = new List<string> { "one", "two", "three", "four" };
string prelast = lines[^2];
Console.WriteLine(prelast);  // output: three
 ```
- .. (range): to specify a range of indices that you can use to obtain a range of sequence elements
```cSharp
int[] numbers = new[] { 0, 10, 20, 30, 40, 50 };
int start = 1;
int amountToTake = 3;
int[] subset = numbers[start..(start + amountToTake)];
Display(subset);  // output: 10 20 30

int margin = 1;
int[] inner = numbers[margin..^margin];
Display(inner);  // output: 10 20 30 40

string line = "one two three";
int amountToTakeFromEnd = 5;
Range endIndices = ^amountToTakeFromEnd..^0;
string end = line[endIndices];
Console.WriteLine(end);  // output: three
 ```

**Type-testing operators and cast expression (C# reference)**

- **is** operator: to check if the runtime type of an expression is compatible with a given type
```Csharp
int i = 27;
Console.WriteLine(i is System.IFormattable);  // output: True

object iBoxed = i;
```

**Type testing with pattern matching**

```Csharp
int i = 23;
object iBoxed = i;
int? jNullable = 7;
if (iBoxed is int a && jNullable is int b)
{
    Console.WriteLine(a + b);  // output 30
}
```

- **as** operator: to explicitly convert an expression to a given type if its runtime type is compatible with that type
- **cast** expression: to perform an explicit conversion
- **typeof** operator: to obtain the System.Type instance for a type
```Csharp
void PrintType<T>() => Console.WriteLine(typeof(T));

Console.WriteLine(typeof(List<string>));
PrintType<int>();
PrintType<System.Int32>();
```


[1]: <https://www.bbc.co.uk/bitesize/guides/zc6s4wx/revision/5#:~:text=Variables%20are%20data%20values%20that,is%20used%20to%20hold%20data.> "Constants, variables and data types"

[2]: <https://www.geeksforgeeks.org/c-sharp-identifiers/> "C# | Identifiers"

[3]: <https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/operators/boolean-logical-operators/> "Boolean logical operators (C# reference)"

