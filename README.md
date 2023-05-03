Download Link: https://assignmentchef.com/product/solved-cs135-project-3
<br>
<u>Project [3]: Loops</u>




<h1>Project Goals</h1>

The goals of this project are to:

<ol>

 <li>Get students familiar with computing iteration using while and for loops</li>

 <li>Show students how simple it can be to implement complicated-looking programs</li>

</ol>




<strong><u>Important Notes:</u></strong> 1. <strong>Formatting: </strong>Make sure that you follow the precise recommendations for the output content and formatting: for example, do not change to text in the first problem from “Enter a number: ” to “Enter number: ”. Your assignment will be auto-graded and any changes in formatting will result in a loss in the grade.

<ol start="2">

 <li><strong>Comments:</strong> Header comments are required on all files and recommended for the rest of the program. Points will be deducted if no header comments are included.</li>

 <li><strong>Restriction: </strong>The use of goto statements anywhere within this program is prohibited. Points will be deducted if goto is used.</li>

</ol>




<h1>Problem 1</h1>

Write a program to guess the square root of a number. It is possible to calculate the square root of a number (for example 2) by starting with an initial guess and iteratively improving the guess with a simple mathematical operation until the guess is “good enough.” In the case of the square root, the pseudocode to find the square root of a number, n, is:

new_guess &lt;- (old_guess + (n / old_guess)) / 2.0

For example, if we want to find the square root of two using this rule, we start with an initial guess of 1.0 and repeatedly use the rule in a loop to produce the sequence:

1.0, 1.5, 1.41667, 1.41422

The last number in the sequence is very close to the square root of 2. The procedure stops when the square of the guess is close enough to the number entered. How close is close enough? It depends on the application, but for our purposes, if the absolute value of the difference between the input and the squared guess is smaller than 1e-5 then we should consider the guess “good enough.” You should use doubledata type for all variables used in your program.

Write a program that asks the user to enter a positive number. Using the procedure described in the previous paragraph, your program should use a loop to compute the square root of the given number. Your program should use a while loop to achieve this. The loops should stop when the absolute value of the difference between the square of the guess and the input number is smaller than 1e-5, as described in the pseudocode below:

Loop ends when: |(guess)<sup>2</sup> – n| &lt; 1e-5

Your program should print the value of the guess at each iteration. When you print the guess, you should have a minimum of 10 spaces in what you print, and you should print five numbers after the decimal point. For the final answer, you should print five numbers after the decimal point.







The program should function as follows (items underlined are to be entered by the user):

Enter a number: <u>361</u>

1.00000  181.00000

91.49724   47.72136   27.64305   20.35120   19.04486

19.00005

Estimated square root of 361.00000: 19.00000 <strong>Notes:</strong>

<ul>

 <li>For this program, in order to compute absolute values you must use the fabs()function from the math library. To do this:</li>

 <li>Add #include &lt;math.h&gt; in your cfile</li>

 <li>Add -lm to the compilation command: gcc -o sq_root sq_root.c -lm</li>

 <li>To read and print doubles with scanf and printf, you will need to use %lf</li>

</ul>




Save your program as sq_root.c




<strong>Challenge for problem 1 </strong>(10 extra credit points):

We had to use double-precision floating point numbers for this problem because if you use single-precision float point numbers then the procedure described above may sometimes fail to find a solution. The way that it fails is that the program gets “stuck” repeating the same guess over and over. For the challenge problem, change all your double variables into float variables, and add an int variable that counts the number of times you have gone through the body of your while loop, starting at zero. Your program should print both the iteration counter and the guess at each step. Your program should be able to detect the “stuck” case and terminate properly.




The program should function as follows (items underlined are to be entered by the user):

Enter a number: <u>100</u>

<ul>

 <li>00000</li>

 <li>50000</li>

 <li>24010</li>

 <li>02553</li>

 <li>84044</li>

 <li>03258</li>

 <li>00005</li>

</ul>

Estimated square root of 100.00000: 10.00000




The iteration counter column and the guess column should be separated by a tab. When you print the guess, you should have a minimum of 10 spaces in what you print, and you should print five numbers after the decimal point. For the final answer, you should print five numbers after the decimal point.




Save your challenge separately as sq_root_c.c




<h1>Problem 2</h1>

Write a program that asks the user to enter an integer number, n, and computes the following mathematical series:

S = 1<sup>2</sup> – 2<sup>2</sup> + 3<sup>2</sup> – 4<sup>2</sup> +…+ (-1)<sup> n+1 </sup>* n<sup>2</sup> Your program should use a for loop to compute this series.




The program should function as follows (items underlined are to be entered by the user):

Enter an integer number: <u>5</u> The value of the series is: 15




Save your program as series.c





