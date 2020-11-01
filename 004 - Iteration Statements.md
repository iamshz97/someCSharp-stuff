## Iteration Statements

1. For loop
2. Foreach Loop
3. While Loop
4. Do While Loop

- Break : Gets our of loop
- Continue : jump to next iteration

**For loop**

```Csharp
/*
for (initializer; condition; iterator)
    body
*/

for (int i = 0; i < 5; i++)
{
    Console.WriteLine(i);
}
```

**For Each**
```Csharp
var fibNumbers = new List<int> { 0, 1, 1, 2, 3, 5, 8, 13 };
int count = 0;
foreach (int element in fibNumbers)
{
    count++;
    Console.WriteLine($"Element #{count}: {element}");
}
Console.WriteLine($"Number of elements: {count}");
```


**While**
```Csharp
int n = 0;
while (n < 5)
{
    Console.WriteLine(n);
    n++;
}
```

**Do**
Executes atleast ones


```Csharp
int n = 0;
do
{
    Console.WriteLine(n);
    n++;
} while (n < 5);
```