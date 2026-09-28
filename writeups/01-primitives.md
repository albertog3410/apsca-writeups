# Process Writeup
## Name: Alberto Gonzalez Jr
## Course: APSCA
## Period: 1
## Concept: Primitive Types

### Context 
In my first few weeks of APCSA, I learned how to use the basics of storing data using **Primitive Types** like numbers, decimals, and true/false statements (booleans). I also learned how to change these values using arithmetic expressions and how to switch a value from one data type to another using **Type Casting**. At first, I found these lessons to be difficult, but as I took notes while doing assigned courses on <a href ="https://courses.projectstem.org/">projectstem.org</a> strengthened my understanding on the unit. 

### Data Types

There are various data types used to store different characters, such as ``int`` for whole numbers, ``double`` for numbers with decimal points, ``String`` for words and letters and ``boolean`` for holding true and false statements. In order to turn these values into inputs, you would need to use a mechanism that reads the user's input and store it into a variable. We would do this by using ``Scanner`` at the top in order for the computer to receive user input. For the computer to know what kind of user input, you would have to use:

* ``.nextLine()`` - Computer can only accept ``String`` values.
* ``.nextInt()`` - Computer can only accept ``int`` values.
* ``nextDouble()`` - Computer can only accept ``double`` values.
* ``nextBoolean()`` - Computer can only accept ``Boolean`` values.

##### Example 
```js
import java.util.Scanner;
class U1_L2_template
{
  public static void main(String[] args) 
  {
    Scanner scan = new Scanner(System.in);
    String n;
    System.out.println("What is your name?");
    n = scan.nextLine(); // the next line after this would be a user input ex: Alberto
    System.out.println("Hello " + n + ". Nice to meet you"); // would print out Hello Alberto. Nice to meet you
  }
}
```


### Type Casting
Type Casting involves changing the data type of a variable by storing it in another variable. You would do this by placing their value inside of another value’s equation. For example, if I wanted to use an  ``int`` variable(x) into a division equation that is going to end with a mixed number. I could not input that normally into ``System.out.println()`` being that ``int`` can only hold whole numbers, which would result in an error. To fix this, I would have to put the value of (x) into a different type of variable that will hold a double. While also indicating inside the variable that x will be a double by putting ``(double)`` in front of the equation. 
```js
int x = 13; 
double half = (double)x / 2;
System.out.println(half); // would print out 6.5
```

### Challenge I Had With Moduclar Division
Starting this, I did not really understand the concept of ``%`` or Mod being that I felt that I did not need to use it much. So when it came to doing an entire lesson based on Moduclar Division, I was stuck. For one of the coding activities, I had to print out each number of a three digit integer and print them from hundreds place to ones. I got confused on how to get the number of the ten's place. Due to this, I decided to look back on at the introduction page to get a better idea on what mod does. That was when I learned that mod was not just normal division, it was the remainder of a division equation. So in order to get the second number, I had to mod the number by 100 then divide by ten. For example, lets say I had the number 678 and I wanted the 7 in that number. Dividing this number by 100 would leave me with 78, but in order to get the 7, I would have to divide 78 by 10, leaving me with 7.8. Due to the input already being declared as an `int` data type, the computer would only print out 7, not 7.8. 

##### Solution
```js
/* Unit 1 - Lesson 5 - Coding Activity Question 1 */

import java.util.Scanner;

class U1_L5_Activity_One 
{
    public static void main(String[] args) 
    {
      
       /* Write your code here */
      Scanner intgers = new Scanner(System.in);
      System.out.println("Please enter a three digit number:");
      int userInput = intgers.nextInt();
      System.out.println("Here are the digits:");
      System.out.println(userInput / 100);
      System.out.println((userInput % 100) / 10);
      System.out.println(userInput % 10);
      
    }
}
```


### Takeaways
From this course, I learned more about concepts of arithmetic equations than I expected to learn. Not just about Java, but also on how I should process these next units so I won't remain stuck. 

* I learned how to use ``%`` in order to find the remainder of a division equation. Even though I have seen ``%`` used in arthimatic problems before, I never bothered to learn more about it. Now I see the use for this operator symbol, not just in coding but in coding and problem solving.
* I learned to **Pay Attention to Detail** whenever I am learning something new. Whether it is something that you don't think it important, even one line of code serves a purpose in the entire system. Which is something I learned when discovering ``%``.
* **Problem Decomposition** - When solving the lesson about mod, I had to take my time and picture how the math would have to play out in order for the second number in the three digit integer to be outputted. If I hadn't done this, I probably would have been stuck for a longer time.









