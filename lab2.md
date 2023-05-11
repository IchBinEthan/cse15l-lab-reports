# Lab Report 2

## Part 1 -- StringSearch.java 

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cse15Lab2stringSearch.png)

Here is how I did the assignment for  `StringSearch.java`. For this lab I used the code from the files in wavelet after forking it on Github. 

* I attempt to use the `add-message` path to add messages onto the file. 
* For this, I had cited code from the `NumberSearch.java` file. In this file, I obtain some code from the  `handler` method in order to write another method in StringSearch.java for the same purpose -- only now, from every query I am extracting I seek to get a String. 
*  This entails defining a empty String `input` with the same logic for extraction of the query from the URL: get the query, splice by `"="`, make sure the first part of which equals the string `"s"` so that the code can run, appending second part (the actual query) to the `input` string. 
* The examples below show how the code would run. After compiling, here is what would happen if I had the two following inputs `Coffee` and  `Yes, I said Coffee` in the query of the URL. 

In this screenshot I added a message with the `add-message` path. Here is the instance of me calling the `add-message` path to add the query `Coffee`.  
![Image](https://ichbinethan.github.io/cse15l-lab-reports/cse15Lab2coffee.png)

In this screenshot, I added the message `Yes, I said Coffee` by using the same command `add-message`. Here, we see in this instance that the query is `Yes, I said Coffee`, which is then added on the next line under the first message I put in. 
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
  
  Here are implementations of the method before and after it was debugged in these JUnit tests:
  
  ![Image](https://ichbinethan.github.io/cse15l-lab-reports/cse15Lab2fail.png)
  ![Image](https://ichbinethan.github.io/cse15l-lab-reports/cse15Lab2pass.png)
  
  * We can see here that I needed to write the test correctly in order to properly evaluate. We are dealing with a void method, therefore the tests need to account for this. I did not make a new array to evaluate the result because there is no result at all to check using the method.
  * The key idea for this is to figure out how to arrange this in such a way that the code can run without any contradictions or repeats of past assignments. I originally wanted to take the element assigned at index `length - i - 1` and assign to index `i`, but the code wouldn't work because the result would be a split, symmetrical array from the middle. 
  * The idea is -- I define a `temp` variable to store the beginning element, do the assignment of the rest of the spots, then the spot on the very end, indexed at `arr.length - i - 1`, will get assigned whatever is in the temp variable. 
  * This should only get done only half the number of times. 
  
  Here is a passing test:
  ```
    @Test 
  public void testReversed1(){
    int[] exArray = new int[]{20, 19, 18, 17, 16};
    int[] exResult = new int[]{16, 17, 18, 19, 20};
    assertArrayEquals(ArrayExamples.reversed(exArray), exResult);
  }
  ```
  
  Here is a failing test:
  ```
    @Test 
  public void testReverseInPlace1(){
    int[] exInput = new int[]{1, 2, 3, 4};
    int[] exInput = new int[]{4, 3, 2, 1};
    assertArrayEquals(exOutput, ArrayExamples.reverseInPlace(exInput));
  }
  ```
The reason why this one fails is because the test for reverseInPlace assumes that the method isn't void. We comnpare results of arrays from a void method attempting to give a result. This is a contradiction and therefore the test doesn't pass. 



## Part 3 -- Anything New?

I learned more about debugging code and trying to figure out how to use more effective strategies in debugging. I understand and learned that the process is very frustrating at times, but such is the life of a CS student. I think the usage of the temp variable was very intuitive, shoutout to the TA that helped me with that :)
