# cs252-project-3-solved
**TO GET THIS SOLUTION VISIT:** [CS252 Project #3 Solved](https://www.ankitcodinghub.com/product/cs-252-fall-23-computer-organization-solved-3/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;120278&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS252 Project #3 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Assembly Project #3

1 Purpose

In this Project, we’ll be using functions for the first time . You will implement several different functions, which can be called by the testcases; some of those functions will have to call other functions.

1.1 Required Filenames to Turn in

Name your assembly language file asm3.s.

1.2 Allowable Instructions

When writing MIPS assembly, the only instructions that you are allowed to use (so far) are:

add, addi, sub, addu, addiu and, andi, or, ori, xor, xori, nor beq, bne, j jal, jr slt, slti sll, sra, srl lw, lh, lb, sw, sh, sb

la syscall

While MIPS has many other useful instructions (and the assembler recognizes many pseudo-instructions), do not use them! We want you to learn the fundamentals of how assembly language works – you can use fancy tricks after this class is over.

2 No Standard Wrapper

There’s no standard wrapper for this project; you will be writing several independent functions. But it might be interesting to go back to the Asm 2 spec, and see what you’ve been doing. By now, you have the information necessary to understand what studentMain() was.

3 Tasks

Your file must declare a set of functions, as detailed below. In this project, you won’t have any global variables provided by the testcase; instead, everything that you need to know will be provided through parameters.

(In the descriptions below, I’ve described some of the functions by giving you C code; I’ve described others using words. Of course, you’ll be writing MIPS assembly for all of them!)

(spec continues on the next page)

3.1 Task 1: Collatz, Part 1

The Collatz Conjecture (https://en.wikipedia.org/wiki/Collatz_conjecture) is a fun little property of integers; it has been shown to be true for many positive integers – but nobody yet knows if it is true for all positive integers. In this function, you’ll model part of it – the part where an even number is divided down, many times, until you find an odd number underneath.

int collatz_line(int val)

{

if (val % 2 == 1) // is the value odd?

{ printf(“%d “, val); return val;

} printf(“%d”, val);

int cur = val; while (cur % 2 == 0)

{

cur /= 2; printf(” %d”, cur);

}

printf(” “); return cur; }

(spec continues on the next page)

3.2 Task 2: Collatz, Part 2

This will model the Collatz Conjecture for a certain number, all the way down until it hits 1.

Convert the following C function to MIPS assembly:

void collatz(int val)

{

int cur = val; int calls = 0; cur = collatz_line(cur);

while (cur != 1)

{ cur = 3*cur+1; cur = collatz_line(cur); calls++;

}

printf(“collatz(%d) completed after %d calls to collatz_line(). “, val, calls); printf(” “);

}

Remember that printf() is not available in MIPS; you’ll have to do syscalls.

3.3 Task 3: Find the % Character

For this task, declare a function named percentSearch(). This function takes a single parameter, which is a string . It returns an int.

Search the string for the first percent sign (’%’). If you find one, return the index of that character. If not, then return -1.

(spec continues on the next page)

3.4 Task 4: A Tree of Letters

Convert the following C function to MIPS assembly:

int letterTree(int step)

{

int count = 0; int pos = 0;

while (1) // we’ll break out manually, when required

{ char c = getNextLetter(pos); if (c == ’’) // this is literally *ZERO* break;

for (int i=0; i&lt;=count; i++)

printf(“%c”, c); // use syscall 11

printf(” “);

count++; pos += step;

}

return pos;

}

The prototype for getNextLetter() is as follows:

char getNextLetter(int);

3.5 Requirement: Don’t Assume Memory Layout!

To make sure that you don’t make this mistake, we will include testcases that have the variables in many different orders.

4 Running Your Code

You should always run your code using the grading script before you turn it in. However, while you are writing (or debugging) your code, it often handy to run the code yourself.

4.1 Running With Mars (GUI)

This will open a GUI, where you can edit and then run your code. Put your code, plus one testcase, in some directory. Open your code in the Mars editor; you can edit it there. When it’s ready to run, assemble it (F3), run it (F5), or step through it one instruction at a time (F7). You can even step backwards in time (F8)!

4.1.1 Running the Mars GUI the First Time

The first time that you run the Mars GUI, you will need to go into the Settings menu, and set two options:

Assemble all files in directory – so your code will find, and link with, the testcase

Initialize Program Counter to ’main’ if defined – so that the program will begin with main() (in the testcase) instead of the first line of code in your file.

4.2 Running Mars at the Command Line

You can also run Mars without a GUI. This will only print out the things that you explicitly print inside your program (and errors, of course). However, it’s an easy way to test simple fixes. (And of course, it’s how the grading script works.) Perhaps the nicest part of it is that (unlike the GUI, as far as I can tell), you can tell Mars exactly what files you want to run – so multiple testcases in the directory is OK.

To run Mars at the command line, type the following command:

java -jar &lt;marsJarFileName&gt; sm &lt;testcaseName&gt;.s &lt;yourSolution&gt;.s

5 A Note About Grading

Your code will be tested automatically. Therefore, your code must:

Use exactly the filenames that we specify (remember that names are case sensitive).

Not use any other files (unless allowed by the project spec) – since our grading script won’t know to use them.

Follow the spec precisely (don’t change any names, or edit the files I give you, unless the spec says to do so).

(In projects that require output) match the required output exactly! Any extra spaces, blank lines misspelled words, etc. will cause the testcase to fail.

To make it easy to check, I have provided the grading script. I strongly recommend that you download the grading script and all of the testcases, and use them to test your code from the beginning. You want to detect any problems early on!

5.1 Testcases

For assembly language programs, the testcases will be named test *.s . For C programs, the testcases will be named test *.c . For Java programs, the testcases will be named Test *.java . (You will only have testcases for the languages that you have to actually write for each project, of course.)

Each testcase has a matching output file, which ends in .out; our grading script needs to have both files available in order to test your code.

5.2 Automatic Testing

We have provided a testing script (in the same directory), named grade asm3, along with a helper script, mips checker.pl. Place both scripts, all of the testcase files (including their .out files), and your program files in the same directory. (I recommend that you do this on Lectura, or a similar department machine. It might also work on your Mac or Linux box, but no promises!)

5.3 Writing Your Own Testcases

The grading script will grade your code based on the testcases it finds in the current directory. Start with the testcases I provide – however, I encourage you to write your own as well. If you write your own, simply name your testcases using the same pattern as mine, and the grading script will pick them up.

6 Turning in Your Solution

You must turn in your code to GradeScope. Turn in only your program; do not turn in any testcases or other files.
