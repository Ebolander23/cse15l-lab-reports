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
![Image](failure.png)

4) testReversedFailure(ArrayTests)
arrays first differed at element [0]; expected:<5> but was:<0>
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:78)
        at org.junit.internal.ComparisonCriteria.arrayEquals(ComparisonCriteria.java:28)
        at org.junit.Assert.internalArrayEquals(Assert.java:534)
        at org.junit.Assert.assertArrayEquals(Assert.java:418)
        at org.junit.Assert.assertArrayEquals(Assert.java:429)
        at ArrayTests.testReversedFailure(ArrayTests.java:34)

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

## Grep Research: 

  1. `grep -r` (or --recursive): Search recursively through directories
     Searches for a pattern within all files "search_term" within the technical directory:
     ```
     grep -r "parasitic" ./technical
./technical/biomed/1471-2148-1-8.txt:            relationships between free-living and parasitic
./technical/biomed/1471-2148-1-8.txt:            the free-living or the parasitic bacterial cluster,
./technical/biomed/1471-2148-1-8.txt:            parasitic species [ 8 9 ] . Such an operation could be
./technical/biomed/1471-2148-1-8.txt:            parasitic bacteria despite major differences in gene
```
     Search and Display Line Numbers that contain the key term "search_term":
     ```
    grep -rn "parasitic" ./technical
./technical/biomed/1471-2148-1-8.txt:247:            relationships between free-living and parasitic
./technical/biomed/1471-2148-1-8.txt:258:            the free-living or the parasitic bacterial cluster,
```
     
 
 2.  `grep -c` prints count of lines matching criteria
    ```
     grep -c "parasite" ./technical/biomed/1468-6708-3-1.txt
0
```
```
grep -c "Cardiovascular" ./technical/biomed/1468-6708-3-1.txt
3
```
     

 
3.  `grep -v` (or --invert-match): Display non-matching lines
     This command shows lines in txt file that excludes the pattern specified:
     ```
grep -v "Cardiovascular" ./technical/biomed/1468-6708-3-1.txt
Introduction
        Older adults are frequently counseled to lose weight,
        even though there is little evidence that overweight is
```
`grep -vc` counts amount of lines that don't match
```
grep -vc "Cardiovascular" ./technical/biomed/1468-6708-3-1.txt
```
     
  
 4. `grep -A n` (or --after-context): Display lines after the matched line
     This command shows the pattern specified, plus the next n lines:
    ```
    grep -A 3 "crash" ./technical/911report/chapter-1.txt
    At 8:46:40, American 11 crashed into the North Tower of the World Trade Center in New York City.

    All on board, along with an unknown number of people in the tower, were killed instantly.
    ```
    ```
    grep -A 0 "crash" ./technical/911report/chapter-1.txt
    At 8:46:40, American 11 crashed into the North Tower of the World Trade Center in New York City
    ```

--


        
 
