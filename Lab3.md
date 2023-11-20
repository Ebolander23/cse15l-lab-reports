# Lab 3 - Eric Bolander
## Bug to Fix: Reversed Array 
```
# code block
@Test
  public void testReversedNoFailure() {
    int[] inputArray = {5, 4, 3, 2, 1};
    int[] expectedResult = {1, 2, 3, 4, 5};
    int[] result = YourClass.reversed(inputArray);
    assertArrayEquals(expectedResult, result);
  }
java -cp ".;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore ArrayTests
```
```
# code block
@Test
  public void testReversedNoFailure() {
    int[] inputArray = {5, 4, 3, 2, 1};
    int[] expectedResult = {1, 2, 3, 4, 5};
    int[] result = YourClass.reversed(inputArray);
    assertArrayEquals(expectedResult, result);
  }
java -cp ".;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore ArrayTests
```
## Failure Inducing output: 
![Image](imageName.png)

## Bug Before the Fix: 
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
        arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
}
## Bug After Fix: 
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
        newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
}
## Explanation: 
 The loop is overwriting the values in the arr array with the reversed values of the newArray. The assignment of variables has to be reversed. 

```
# code block
  1. -r (or --recursive): Search recursively through directories
     Searches for a pattern within all files "search_term" within the technical directory:
     grep -r "search_term" ./technical
     Search and Display Line Numbers that contain the key term "search_term":
     grep -rn "search_term" ./technical
```
 ```
# code block
 2.  -i (or --ignore-case): Perform case-insensitive search
     Command that ignores the case of the letters and searches in the 1.txt file of technical:
     grep -i "pattern" ./technical/1.txt
     Command that is not case sensitive, and also displays line numbers associated with specified pattern:
     grep -in "pattern" ./technical/1.txt
```
```
  # code block
3.  -v (or --invert-match): Display non-matching lines
     This command shows lines in 1.txt file that excludes the pattern specified:
     grep -v "exclude_pattern" ./technical/1.txt
     This command shows lines in ALL files of technical that exclude the specified pattern:
     grep -vr "exclude_pattern" ./technical
```
 ```
  # code block
 4. -A (or --after-context): Display lines after the matched line
     This command shows the pattern specified, plus the next 3 lines: 
     grep -A 3 "pattern" ./technical/1.txt
     This command shows the lines after the pattern is found that you specified:
     grep -Ar 3 "pattern" ./technical
```
        
 
