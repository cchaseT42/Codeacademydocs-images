---
Title: "Arrays"
Subjects:
  - "Code Foundations"
  - "Computer Science"
Tags:
  - "Arrays"
  - "Lists"
  - "Variable Types"
CatalogContent:
  - "learn-c-plus-plus"
  - "paths/computer-science"
---

In the C language, an array is a list of values, with a fixed length.  

Being able to store multiple pieces of related information in the same structure is very useful when writing C programs.

## Declaring an Array

The syntax for declaring an array is first specify the data type, then a descriptive array name, followed by square brackets surrounding the array's length (number of items):

```pseudo
type name[length];
```

So to declare an `int` array named `grades` with a length of 5:

```c
int grades[5]; // An array to hold five integers
```

Alternatively, the length can be omitted and the array's initial values can be assigned to it instead. Values are assigned inside of the curly brackets and separated by commas.

```c
int grades[] = {94, 90, 78, 82, 88};
```

## Accessing Values

The values in arrays are accessed using their index, or their position in the array. They can either be assigned or used this way.

```c
char vowels[] = {'a', 'e', 'i', 'o', 'u'}; 
```

Note that in C, an array's indexes start at 0 instead of 1:

```pseudo
      +-------------------------+
Value | 'a'  'e'  'i'  'o'  'u' |
      +-------------------------+
Index |  0    1    2    3    4  |
      +-------------------------+
```

- `vowels[0]` will give use the value `'a'`.
- `vowels[1]` will give use the value `'e'`.
- `vowels[2]` will give use the value `'i'`.
- `vowels[3]` will give use the value `'o'`.
- `vowels[4]` will give use the value `'u'`.


```c
char vowels[] = {'a', 'e', 'i', 'o', 'u'};

printf("%c", vowels[3]); 
// Output: o
```

## Example

```c
#include <stdio.h>

int main(void) {
  int nums[] = {1, 2, 3, 4, 5};
  
  printf("%d\n", nums[0]);
  
  nums[3] = 17;
  
  printf("%d\n", nums[3]);

  return 0;
}
```

The output would be:

```shell
1
17
```