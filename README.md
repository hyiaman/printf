## Printf Group project
This is a collaboration project to create a user-defined printf function.
printf is the C language function to do formatted printing.

## Origin
In the early days, computer programmers would write their own subroutines to read in and print out numbers. 
Eventually the most popular of these functions were canonized into membership in the “standard” libraries. 
Number printing was popular enough to gain this hallowed honor.
This meant that programmers did not have to reinvent the number-printing subroutine again and again. 
It also meant that everybody’s favorite options tried to make it into the standard.
Thus was printf born.

## Simple printing
Usually the most simple case, printf takes one argument: a string of characters to be printed. This string is composed of characters, each of which is printed exactly as it appears. So printf("xyz"); would simply print an x, then a y, and finally a z. This is not exactly “formatted” printing, but it is still the basis of what printf does.

## Special Characters
To identify the start of the string, we put a doublequote (") at the front. To identify the end of the string we put another double-quote at the end. This bears the questions, what if we want to print the doublequote itself??
The normal print what you see does not apply to these special characters like doublequote. Thus, to print a doublequote you type in backslash double-quote. To print a backslash, you must escape it by typing another backslash in front of it. The first backslash means “give the next character its alternate meaning.” The second backslash has an alternate meaning of “print a backslash.”
Without a backslash, special characters have a natural special meaning. With a backslash they print as they appear. Here is a partial list.

```
\ 	escape the next character
\\ 	print a backslash
" 	start or end of string
\" 	print a double quote
’ 	start or end a character constant
\’ 	print a single quote
% 	start a format specification
\% 	print a percent sign
```

## Format Specification
The real power of printf is when we are printing the contents of variables. Let’s take the format specifier %d for example. This prints a number. So, a nummber must be provided for printing. This is done by adding another argument to the printf statement, as shown here.


```
int age;
age = 25;
printf ( "I am %d years old\n", age );
```
In this example, printf has two arguments. The first is a string: "I am %d years old\n". The second is an integer, age.

## Argument List
When printf processes its arguments, it starts printing the characters it finds in the first argument, one by one. When it finds a percent it knows it has a format specification. It goes to the next argument and uses its value, printing it according to that format specification. It then returns to printing a character at a time (from the first argument). Below is a sample list of arguments:  
```
%c  print a single character
%d  print a decimal (base 10) number
%e  print an exponential floating-point number
%f  print a floating-point number
%g  print a general-format floating-point number
%i  print an integer in base 10
%o  print a number in octal (base 8)
%s  print a string of characters
%u  print an unsigned decimal (base 10) number
```
## Conclusion
The printf function is a powerful device for printing numbers and other things stored in variables. With this power there is a certain amount of complexity. Taken all at once, the complexity makes printf seem almost impossible to understand. But the complexity can be easily unfolded into simple features, including width, precision, signage, justification, and fill.

This customized printf function can mimic all the above listed behaviour of the standard printf as described above.