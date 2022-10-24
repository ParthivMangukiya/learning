# Clean Code

## Chapter 1: Clean Code

> Clean code can be read and enhance by the the developers other than its auther. 
>
> <cite> - "Big" Dave Thomas<cite>

> Clean code is Simple and Direct. Clean code never obscures designer's intent.
> 
> <cite>- Grady Booch</cite>

**The Boy Scount Rule**

> Leave the campground cleaner than you found it.

**We are Authors**

The ratio of time spent reading vs. writing code is well over 10:1. Easy to read code -> Easy to write code. 


## Chapter 2: Meaningful Names

### Distinction between Simplicy and Implicity

- Simple yet Not Implicit

    ````c++
    public static void copy(char a1[], char a2[]) {
        for (int i=0; i< a1.length; i++) {
            a2[i] = a1[i];
        }
    }
    ```

- Implicit Code

    ```c++
    public static void copyString(char source[], char destination[]) {
        for (int i=0; i< source.length; i++) {
            destination[i] = source[i];
        }
    }
    ```

### Avoid Disinformation

- Grouping of accounts - do not name it as `accountList` instead name it as `accountGroup` (List for Programmers means Actual Data Structures)
- Do not use names which very in small ways. e.g. `XYZControllerForEfficientHandlingOfStrings` and `XYZControllerForEfficientStorageOfStrings`
-  Do not name `FullState` as `fs`

### Make Meaningful Distinciton

- Do not add Noise words 
    - `ProductInfo` <->`ProductData`
    - `Name` <-> `NameString`
    - `Customer` <-> `CustomerObject` <-> `CustomerInfo`

### Use Pronounceable Names

- `genymdhms` (generation year month date hour minute second) <-> `generationTimestamp`
- `modymdhms` (generation year month date hour minute second) <-> `modificaitonTimestamp` 

## Use Searchable Names

- `MAX_CLASSES_PER_STUDENT` vs `7` (7 is very hard to find in project)



