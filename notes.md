Analytical Engine Presentation

History of the Engine
* The difference engine was a machine designed to find the solution to equations in the form a + bx + cx^2 + ... + hx^7
* Designed difference engine no. 2 in 1849 and constructed at the Science Museum in London between 1989 and 1991
* Describe difference engine and give quote by Ada: The Analytical Engine, on the contrary, is not merely adapted for tabulating the results of one particular function and of no other, but for developing and tabulating any function whatever. In fact the engine may be described as being the material expression of any indefinite function of any degree of generality and complexity…
* https://youtu.be/BlbQsKpq3Ak?t=13m24s
* Analytical Engine first described in 1837 as a successor to the difference engine no. 1
* Babbage was famous for his "Table of Logarithms of the Natural Numbers" and he envisioned the analytical engine as being able to compute these log tables. There was a big problem with misprintings in the log books, and the analytical engine would solve this.
* Never built
* Top illustration
* Front illustration

What the Engine Means for History
* Turing Completeness, what is it?
* Abstract data representations: Ada quote: [The Analytical Engine] might act upon other things besides number, were objects found whose mutual fundamental relations could be expressed by those of the abstract science of operations, and which should be also susceptible of adaptations to the action of the operating notation and mechanism of the engine...Supposing, for instance, that the fundamental relations of pitched sounds in the science of harmony and of musical composition were susceptible of such expression and adaptations, the engine might compose elaborate and scientific pieces of music of any degree of complexity or extent.
* First imaginings of algorithmic efficiency. Babbage: "As soon as an Analytical Engine exists, it will necessarily guide the future course of the science. Whenever any result is sought by its aid, the question will then arise—By what course of calculation can these results be arrived at by the machine in the shortest time?"

How the Engine Works
* Harvard Architecture (Completely separate memory and instructions, instructions aren't even read into memory, unlike today's Modified Harvard Architecture where instructions are stored in memory but aren't readily accessed. The instructions roller is litterally rolled forward and backward)
* Unlike difference engine, this would have required a steam engine to run instead of a hand crank.
* Annunciator Panel: Panel where Attendant would monitor the machine
* Printer: Prints results both on paper and supposedly in plaster, for future replication
* Curve Drawing Apparatus: Consists of a pen hovering above a sheet, useful for drawing function curves. Babbage: “The discovery of laws from the examination of a multitude of tabulated and reduced observations is greatly assisted by the representation of such tables in the form of curves.”
* Attendant: Human responsible for library and conditional expansion
* Mill: CPU of the Engine, responsible for doing all operations according to a series of instruction drums. Mill's lever is triggered during a subtraction that results in a negative number, and is used in conditional statements. Has two ingress axis, a primed ingress axis (for loading in numbers that are more than 50 significant digits for certain operations), an egress axis, and a primed egress axis (for certain extra numbers, like the quotient of division)
* Card Reader: Used thick punch cards not unlike Jacquard loom. Could advance and backtrack
* Store: 1000 columns of 50 digit numbers. Represents 166kb of memory when converted to binary. More than the IBM 1401

Porting the Engine
* John Walker wrote the first emulator in 1997 as a Java applet, ported in 2017 to JavaScript

Writing for the Engine
* Commands and numbers
	* A xxxxxxxxxxx attendant instructions
	* . xxxxxxxxxxx comments
	* NXXX YYY Set the store at XXX to value YYY
	* {}(){?(? Skips, loops, and conditionals of each
	* -+/* operators
	* LXXX load number at store location XXX into mill. If this is the second load after an operator, execute function
	* SXXX save number in egress axis at store position XXX
* Explain how a simple addition and save would be performed
	* N000 1
	* N001 2
	* +
	* L000
	* L001
	* S002
* Demo of atom language package for programming
* Metaprogramming to introduce pointers and string printing
* Patterns
* Reliance on the Assistant and Libraries

Demos
* Demo of mandelbrot viewer
