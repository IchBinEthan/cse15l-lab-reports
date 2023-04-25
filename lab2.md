# Lab Report 2

## Part 1 -- StringSearch.java

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cse15Lab2stringSearch.png)

Here is how I did the assignment for  `StringSearch.java`. For this lab I used the code from the files in wavelet after forking it on Github. 

* I attempt to use the `add-message` path to add messages onto the file. 
* For this, I had cited code from the `NumberSearch.java` file. In this file, I obtain some code from the  `handler` method in order to write another method in StringSearch.java for the same purpose -- only now, from every query I am extracting I seek to get a String. 
*  This entails defining a empty String `input` with the same logic for extraction of the query from the URL: get the query, splice by `"="`, make sure the first part of which equals the string `"s"` so that the code can run, appending second part (the actual query) to the `input` string. 
* The examples below show how the code would run. After compiling, here is what would happen if I had the two following inputs `Coffee` and  `Yes, I said Coffee` in the query of the URL. 

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cse15Lab2coffee.png)
![Image](https://ichbinethan.github.io/cse15l-lab-reports/cse15Lab2coffeeMore.png)

## Part 2 -- Debugging

I attempt to debug some of the code in Lab 3, focusing on the `reverseInPlace` method. 

Before:
```
  // Changes the input array to be in reversed order
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  } 
  ```
  
  After:
  ```
    static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length/2; i += 1) {
      int temp = arr[i];
      arr[i] = arr[arr.length - i - 1];
      arr[arr.length - i - 1] = temp;
    } 
  }
  ```
  Here is a passing test:
  ```
    @Test 
  public void testReversed1(){
    int[] exArray = new int[]{20, 19, 18, 17, 16};
    int[] exResult = new int[]{16, 17, 18, 19, 20};
    assertArrayEquals(ArrayExamples.reversed(exArray), exResult);
  }
  ```




## Part 3 -- Anything New?
