- Compilation – the source program is translated once (however, this act must be repeated each time you modify the source code) by getting a file (e.g., an .exe file if the code is intended to be run under MS Windows) containing the machine code. Now you can distribute the file worldwide; the program that performs this translation is called a compiler or translator.

-Interpretation – you (or any user of the code) can translate the source program each time it has to be run. The program performing this kind of transformation is called an interpreter, as it interprets the code every time it is intended to be executed. It also means that you cannot just distribute the source code as-is, because the end-user also needs the interpreter to execute it

-What does this all mean for you?

Python is an interpreted language. This means that it inherits all the described advantages and disadvantages. Of course, it adds some of its unique features to both sets.
If you want to program in Python, you'll need the Python interpreter. You won't be able to run your code without it. Fortunately, Python is free. This is one of its most important advantages.
Due to historical reasons, languages designed to be utilized in the interpretation manner are often called scripting languages, while the source programs encoded using them are called scripts. Okay, let's meet Python.

- A function (in this context) is a separate part of the computer code able to:

cause some effect (e.g., send text to the terminal, create a file, draw an image, play a sound, etc.); this is something completely unheard of in the world of mathematics;
evaluate a value (e.g., the square root of a value or the length of a given text) and return it as the function's result; this is what makes Python functions the relatives of mathematical concepts.

- As we said before, a function may have:

an effect;
a result.
There's also a third, very important, function component ‒ the argument(s).

Mathematical functions usually take one argument. For example, sin(x) takes an x, which is the measure of an angle.

Python functions, on the other hand, are more versatile. Depending on the individual needs, they may accept any number of arguments ‒ as many as necessary to perform their tasks. Note: When we said any number, that includes zero ‒ some Python functions don't need any argument.

***
print("Hello, World!")
***

In spite of the number of needed/provided arguments, Python functions strongly demand the presence of a pair of parentheses ‒ opening and closing ones, respectively.

If you want to deliver one or more arguments to a function, you place them inside the parentheses. If you're going to use a function which doesn't take any argument, you still have to have the parentheses.

Note: to distinguish ordinary words from function names, place a pair of empty parentheses after their names, even if the corresponding function wants one or more arguments. This is a standard convention.

- Unlike most programming languages, Python requires that there cannot be more than one instruction in a line.

- \n
Interestingly, while you can see two characters, Python sees one.

The backslash (\) has a very special meaning when used inside strings ‒ this is called the escape character.

The letter n placed after the backslash comes from the word newline.

- Two conclusions emerge from this example:

a print() function invoked with more than one argument outputs them all on one line;
the print() function puts a space between the outputted arguments on its own initiative.

- *The way in which we are passing the arguments into the print() function is the most common in Python, and is called the positional way. This name comes from the fact that the meaning of the argument is dictated by its position (e.g., the second argument will be outputted after the first, not the other way round).

- The print() function has two keyword arguments that you can use for your purposes. The first is called end.

- In order to use it, it is necessary to know some rules:

a keyword argument consists of three elements: a keyword identifying the argument (end here); an equal sign (=); and a value assigned to that argument;
any keyword arguments have to be put after the last positional argument (this is very important)

* 2.2.1 Literals – the data in itself
- A literal is data whose values are determined by the literal itself.

- You use literals to encode data and to put them into your code. We're now going to show you some conventions you have to obey when using Python.

- the numbers handled by modern computers are of two types:

integers, that is, those which are devoid of the fractional part;
and floating-point numbers (or simply floats), that contain (or are able to contain) the fractional part.


- The characteristic of the numeric value which determines its kind, range, and application, is called the type.

- Note     *Python 3.6 has introduced underscores in numeric literals, allowing for the placement of single underscores between digits and after base specifiers for improved readability. This feature is not available in older versions of Python.

- Octal and hexadecimal numbers
There are two additional conventions in Python that are unknown to the world of mathematics. The first allows us to use numbers in an octal representation.

If an integer number is preceded by an 0O or 0o prefix (zero-o), it will be treated as an octal value. This means that the number must contain digits taken from the [0..7] range only.

0o123 is an octal number with a (decimal) value equal to 83.

The print() function does the conversion automatically. Try this:


***
print(0o123)
***

- The second convention allows us to use hexadecimal numbers. Such numbers should be preceded by the prefix 0x or 0X (zero-x).

0x123 is a hexadecimal number with a (decimal) value equal to 291. The print() function can manage these values too. Try this:

***
Print(0x123)
***

- Extra  

There is one more, special literal that is used in Python: the None literal. This literal is a NoneType object, and it is used to represent the absence of a value. We'll tell you more about it soon.

- 

2.3.2 Basic operators
An operator is a symbol of the programming language, which is able to operate on the values.

-
Remember: Data and operators when connected together form expressions. The simplest expression is a literal itself.

-
Remember: It's possible to formulate the following rules based on this result:

when both ** arguments are integers, the result is an integer, too;
when at least one ** argument is a float, the result is a float, too.

-
The result produced by the division operator is always a float, regardless of whether or not the result seems to be a float at first glance: 1 / 2, or if it looks like a pure integer: 2 / 1.

-
This is very important: rounding always goes to the lesser integer.

-
Integer division can also be called floor division. You will definitely come across this term in the future.

-
Integer division can also be called floor division. You will definitely come across this term in the future.

- Remainder (modulo)
The next operator is quite a peculiar one, because it has no equivalent among traditional arithmetic operators.

Its graphical representation in Python is the % (percent) sign, which may look a bit confusing.

Try to think of it as a slash (division operator) accompanied by two funny little circles.

The result of the operator is a remainder left after the integer division.

In other words, it's the value left over after dividing one value by another to produce an integer quotient

- Operators and their bindings
The binding of the operator determines the order of computations performed by some operators with equal priority, put side by side in one expression.

- The two possible results are:

***
2  2 → 4; 4  3 → 64
2  3 → 8; 2  8 → 256
***

Run the code. What do you see?

The result clearly shows that the exponentiation operator uses right-sided binding.

- Key takeaways
1. An expression is a combination of values (or variables, operators, calls to functions ‒ you will learn about them soon) which evaluates to a certain value, e.g., 1 + 2.

2. Operators are special symbols or keywords which are able to operate on the values and perform (mathematical) operations, e.g., the * operator multiplies two values: x * y.

3. Arithmetic operators in Python: + (addition), - (subtraction), * (multiplication), / (classic division ‒ always returns a float), % (modulus ‒ divides left operand by right operand and returns the remainder of the operation, e.g., 5 % 2 = 1),  (exponentiation ‒ left operand raised to the power of right operand, e.g., 2  3 = 2 * 2 * 2 = 8), // (floor/integer division ‒ returns a number resulting from division, but rounded down to the nearest whole number, e.g., 3 // 2.0 = 1.0)

4. A unary operator is an operator with only one operand, e.g., -1, or +3.

5. A binary operator is an operator with two operands, e.g., 4 + 5, or 12 % 5.

6. Some operators act before others - the hierarchy of priorities:

the ** operator (exponentiation) has the highest priority;
then the unary + and - (note: a unary operator to the right of the exponentiation operator binds more strongly, for example 4 ** -1 equals 0.25)
then: *, /, and %,
and finally, the lowest priority: binary + and -.
7. Subexpressions in parentheses are always calculated first, e.g., 15 - 1 * (5 * (1 + 2)) = 0.

8. The exponentiation operator uses right-sided binding, e.g., 2  2  3 = 256.




-

2.4.2 Variable names
If you want to give a name to a variable, you must follow some strict rules:

the name of the variable must be composed of upper-case or lower-case letters, digits, and the character _ (underscore)
the name of the variable must begin with a letter;
the underscore character is a letter;
upper- and lower-case letters are treated as different (a little differently than in the real world – Alice and ALICE are the same first names, but in Python they are two different variable names, and consequently, two different variables);
the name of the variable must not be any of Python's reserved words (the keywords – we'll explain more about this soon).
Note that the same restrictions apply to function names.

-
Keywords
Take a look at the list of words that play a very special role in every Python program.

['False', 'None', 'True', 'and', 'as', 'assert', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']

They are called keywords or (more precisely) reserved keywords. They are reserved because you mustn't use them as names: neither for your variables, nor functions, nor any other named entities you want to create.

-
You can use the print() function and combine text and variables using the + operator to output strings and variables. For example:

***
var = "3.8.5"
print("Python version: " + var)
Python version: 3.8.5
***


2.4.6 Solving simple mathematical problems
Now you should be able to construct a short program solving simple mathematical problems such as the Pythagorean theorem:

The square of the hypotenuse is equal to the sum of the squares of the other two sides.

The following code evaluates the length of the hypotenuse (i.e., the longest side of a right-angled triangle, the one opposite of the right angle) using the Pythagorean theorem:


a = 3.0
b = 4.0
c = (a  2 + b  2) ** 0.5
print("c =", c)
 
Note: we need to make use of the ** operator to evaluate the square root as:

√ (x)  = x(½)

and

c = √ a2 + b2 

Can you guess the output of the code?
