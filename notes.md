Analytical Engine Presentation

Overview
* Analytical Engine was designed in 1837 and was the first mechanical computer ever designed, but it was never built.
* Designed by Charles Babbage, who was an English polymath and was especially noteworthy for his series of published log books.
* Ada, Countess of Lovelace, was an English mathematician and writer. She corresponded with Babbage about the Engine and published the first program meant for it.
* Talk will be divided into three parts
* First we will talk about the history of the engine
* Then comes a description of all the parts of the engine
* Then we will go through some code written for the engine, and watch the engine calculate the mandelbrot set

History of the Engine
* The difference engine was a machine designed to use the method of divided differences to find the solution to equations in the form a + bx + cx^2 + ... + hx^7
* Difference engine 0 was built between 1819 and 1822 and was showcased at Babbage's house, where Ada Lovelace viewed it
* Designed difference engine no. 2 in 1849 and constructed at the Science Museum in London between 1989 and 1991
* https://youtu.be/BlbQsKpq3Ak?t=13m24s
* Analytical Engine first described in 1837 as a successor to the difference engine no. 1
* In the notes of a translation of an Italian mathematician's article on the Analytical Engine, Ada describes the difference between the two machines: The Analytical Engine, on the contrary, is not merely adapted for tabulating the results of one particular function and of no other, but for developing and tabulating any function whatever. In fact the engine may be described as being the material expression of any indefinite function of any degree of generality and complexity…
* Babbage was famous for his "Table of Logarithms of the Natural Numbers" and he envisioned the analytical engine as being able to compute these log tables. There was a big problem with misprintings in the log books, originating from both faulty calculations and faulty copying, and the analytical engine would solve this.
* Give an example of multiplication using the tables
* The analytical engine has never been built
* Top illustration
* Front illustration

What the Engine Means for History
* Turing Completeness, what is it? The ability to branch conditionally and to manipulate memory.
* Abstract data representations: Ada quote: [The Analytical Engine] might act upon other things besides number, were objects found whose mutual fundamental relations could be expressed by those of the abstract science of operations, and which should be also susceptible of adaptations to the action of the operating notation and mechanism of the engine...Supposing, for instance, that the fundamental relations of pitched sounds in the science of harmony and of musical composition were susceptible of such expression and adaptations, the engine might compose elaborate and scientific pieces of music of any degree of complexity or extent.
* First imaginings of algorithmic efficiency. Babbage: "As soon as an Analytical Engine exists, it will necessarily guide the future course of the science. Whenever any result is sought by its aid, the question will then arise—By what course of calculation can these results be arrived at by the machine in the shortest time?"

How the Engine Works
* Harvard Architecture (Completely separate memory and instructions, instructions aren't even read into memory, unlike today's Modified Harvard Architecture where instructions are stored in memory but aren't readily accessed. The instructions roller is literally rolled forward and backward)
* Unlike difference engine, this would have required a steam engine to run instead of a hand crank.
* The size was on par with a steam engine, not a car.
* Annunciator Panel: Panel where Attendant would monitor the machine
* Printer: Prints results both on paper and plaster for the flong for stereotype printing. Lead would be poured onto the flong to produce a stereoplate.
* Curve Drawing Apparatus: Consists of a pen hovering above a sheet, useful for drawing function curves. Babbage: “The discovery of laws from the examination of a multitude of tabulated and reduced observations is greatly assisted by the representation of such tables in the form of curves.”
* Mill: CPU of the Engine, responsible for doing all operations according to a series of instruction drums. Mill's lever is triggered during a subtraction that results in a negative number, and is used in conditional statements. Has two ingress axes, for loading in the operands of operations, and an egress axis which receives the result of an operation.
* Card Reader: Used thick punch cards not unlike Jacquard loom. Could advance and backtrack
* Store: 1000 columns of 50 digit numbers. Represents 166kb of memory when converted to binary. More than the IBM 1401
* Attendant: Human responsible for library and conditional expansion. Converts shorthand loops and skips into their versions that reference the exact number of cards needed to be skipped.

Porting the Engine
* John Walker wrote the first emulator in 1997 as a Java applet, ported in 2017 to JavaScript

Writing for the Engine
* Metaprogramming to introduce pointers and string printing
* Patterns
	* No such thing as declaring a number to use on-the-fly, it has to be in the store already. All numbers needed for a program, like 0 for comparisons and 1 for incrementing or decrementing, must be initialized at the beginning of the program.
* Reliance on the Assistant and Libraries

Demos
* Demo of mandelbrot viewer
analytical-engine Library/mandelbrotviewer.ae
