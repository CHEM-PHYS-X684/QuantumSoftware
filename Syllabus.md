# CHEM/PHYS 3684

| | |
| --- | --- |
| **Room:** |  Robeson 116 |
| **Time:** | 11am-11:50pm |
| **Days:** | Tuesday/Thursday |

### Grading
```mermaid
pie showdata
	"Engagement" : 20
	"Quizzes" : 20
	"Assignments":  30
	"Software" : 30
```

### Tentative Schedule
1. [Computer setup](https://education.molssi.org/python-package-best-practices/setup.html)
	- [Instructions for Windows](https://chem-phys-x684.github.io/python-package-best-practices/setup.html#installing-wsl-windows-users-only)
	- **Quiz**: setup_quiz.ipynb 
	- [Shell tutorial](https://swcarpentry.github.io/shell-novice/)
	- [git tutorial](https://education.molssi.org/python-package-best-practices/00-git-and-github.html)
	- **Assignment**: shell.ipynb 
		> Answer the questions in the provided Jupyter notebook to test your proficiency at using shell commands
1. Python
	- [MolSSI Tutorial](https://education.molssi.org/python_scripting_cms/01-introduction/index.html)
	- [w3schools Tutorial](https://www.w3schools.com/python/default.asp)
	- Concepts
		- [Variables and Functions](https://www.w3schools.com/python/python_variables.asp)
			- [Duck Typing and Type hinting](https://chem-phys-x684.github.io/python-package-best-practices/06-type-hinting.html)
		- [Classes](https://www.w3schools.com/python/python_classes.asp)
			- [Inheritance/Polymorphism](https://www.w3schools.com/python/python_inheritance.asp)
	- **Assignment**: bitstring_class.ipynb 
		> Implement a Python class in a Jupyter notebook that implements a "bitstring", i.e., a string of zeros and ones. We will use this later in the class. 
3. [Math review](<Math Review.md>)
	- **Quiz**: Math review
	- Start Jupyter notebook with math example
4. [Quantum Postulates](Postulates/README.md)  
	- TDSE solutions via trotterization
	- **Quiz**: Postulates
4. [Particle in a Box](https://en.wikipedia.org/wiki/Particle_in_a_box)
	- Example of a quantum system
	- **Assignment**: particle_in_a_box.ipynb 
		> Develop a Jupyter notebook that solves and plots solutions for a 1D particle in a box 
2. [Classical Optimization](CSP/README.md)
	- Constraint Satisfaction Problems (CSP)
		- Max-Cut
		- Traveling Salesman
		- [Good overview connecting to Hamiltonians](https://arxiv.org/pdf/1501.07030.pdf)
	- Ising Model
		- Pauli Operators
		- Code Ground state in Notebook
		- **Assignment:** graph_energy.ipynb
			> Develop a Jupyter notebook that finds the ground state (lowest energy) configuration of an arbitrary Ising Hamiltonian, that is defined by a Graph 
	- Monte Carlo 
		- Thermodynamic averages
		- Go through [MolSSI workshop](https://education.molssi.org/python-package-best-practices/) to develop a software package
		- Turn Jupyter functions into Monte Carlo package 
		- **Assignment:** monte_carlo.ipynb
			> Develop a Python package to implement a Monte Carlo simulation of an arbitrary Ising Hamiltonian
1. Quantum Computing
	- Concepts (Qubits, etc)
	- Basic Gates
	- Qiskit
5. Adiabatic State Preparation
	<!-- - Ising $\rightarrow$ Heisenberg  -->
	- adiabatic principle
	- adiabatic principle for Ising
	- **Assignment**: adiabatic_state_prep.ipynb
		> Develop a Jupyter notebook that builds and executes quantum circuits that find the ground states of an arbitrary Ising Hamiltonian

---

# CHEM/PHYS 4684 

| | |
| --- | --- |
| **Room:** |  Robeson 116 |
| **Time:** | 11am-11:50pm |
| **Days:** | Tuesday/Thursday |


### Grading
```mermaid
pie showdata
	"Mentoring/Engagement" : 20
	"Project Proposal" : 20
	"Software Package":  40
	"Project Presentation" : 20
```

### Tentative Schedule
- points:
	- Collaboration is ok, but must be properly credited. I can look at the git commit history, but that's not enough - any collaboration must also be described in the presentation

### Proposal Rubric
Develop and write a 2-3 page proposal(11pt font, single spaced) proposal.

1. **Motivation:**  (30pts) 
   Why should I care about the problem you are focusing on? 
2. **Limits of current approaches or understandings:** (20pts) 
   Are there limits to the current status?
3. **Project Plan:** (30pts) 
   Give a detailed plan of how you will carry out the project. How will you determine if your project is successful?
4. **Timeline:** (10pts) 
   How long do you expect each step to take?
5. **References:** (10pts) 
   Make sure you include a proper bibliography to support any claims you make

### Software Rubric
Create a Python GitHub package that executes what was proposed above
1. **Documentation:** (20pts)
2. **Unit Testing:** (20pts)
3. **Organization:** (20pts)
4. **Examples:** (20pts)
5. **Performance:** (20pts)


### Presentation Rubric
Prepare and deliver a presentation on your project
1. **Motivation:** (20pts)
1. **Correctness:** (30pts)
2. **Clarity of Materials:** (20pts)
2. **Clarity of Narrative:** (30pts)


# Academic Honor System
The Undergraduate Honor Code pledge that each member of the university community agrees to abide by states:

>As a Hokie, I will conduct myself with honor and integrity at all times.  I will not lie, cheat, or steal, nor will I accept the actions of those who do.


Students enrolled in this course are responsible for abiding by the Honor Code. A student who
has doubts about how the Honor Code applies to any assignment is responsible for obtaining
specific guidance from the course instructor before submitting the assignment for evaluation.
Students are strongly discouraged from misusing sites such as Chegg and CourseHero, as well as
misusing ChatGPT and other Generative Artificial Intelligence. Students are strongly
encouraged to consult their faculty members regarding the use of such outside materials as the
misuse of these sources may constitute a violation of the Honor Code. Ignorance of the rules
does not exclude any member of the University community from the requirements and
expectations of the Honor Code.

Academic integrity expectations are the same for online classes as they are for in person classes.
We strongly encourage all instructors to discuss the use of technology, and specifically discuss
areas we know are problematic temptations for students such as ChatGPT, Chegg, CourseHero,
and GroupMe to discourage students from using them. When the semester starts is an
appropriate time in addition to providing a kind reminder before exams and assignments about
expectations related to these sites. Please make your students aware that we are able to
effectively investigate these incidents. If you have any questions about these sites or discussing
them with your students, please do not hesitate to call our office. All university policies and
procedures apply in any Virginia Tech academic environment, and all students are expected to
follow them.

For additional information about the Honor Code, please visit: https://www.honorsystem.vt.edu/


# Statement of Lauren's Promise
**Lauren's Promise:** I will listen and believe you if someone is threatening you.
