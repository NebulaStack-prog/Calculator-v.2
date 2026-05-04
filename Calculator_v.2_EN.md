## **Part 1. Main Document.**

### **1. Title and Basic Information.**

• **Name:** Calculator v.2

• **Purpose:** Project No. 3. Product.

• **Project Phase:** Phase I.

• **Technology Stack:** Python.

• **Project Status:** The second version is fully completed.

### **2. Brief Project Description.**

• The Calculator v.2 project is a multifunctional desktop application in Python with a graphical interface, designed to perform a wide range of mathematical operations.

• The program combines the functions of a basic, engineering, and scientific calculator, providing tools for arithmetic calculations, working with prime numbers, solving equations, trigonometric transformations, and other mathematical tasks in a convenient and modern interface with saved history.

• Unlike the first version, Calculator v.2 includes graph plotting of various types, an improved interface, and enhanced error handling.

### **3. Clear Project Goals.**

• Demonstrate the development of NS in the project domain.

• Create convenience and multifunctionality for the user.

• Expand the NS project portfolio.

### **4. Project Components (Functions).**

• **What is already implemented:**

**4.1** Addition
(a + b)

**4.2** Subtraction
(a – b)

**4.3** Multiplication
(a × b)

**4.4** Division
(a : b)

**4.5** GCD Calculation
(Euclidean Algorithm)

**4.6** LCM Calculation
(Based on GCD)

**4.7** Factorial
(a! = 1 × 2 × 3 × ... × a)

**4.8** Double Factorial
(If a is even: a!! = 2 × 4 × 6 × ... × a)
(If a is odd: a!! = 1 × 3 × 5 × ... × a)

**4.9** Prime Factorization
(a = p₁ × p₂ × ...)

**4.10** Exponentiation
(a^b = a × a × ... × a)

**4.11** Primality Test
(If a number a has only divisors 1 and a, then it is prime; otherwise, it is composite)

**4.12** Logarithms
(logₐ(b))

**4.13** Square Root
(√a = a^0.5)

**4.14** Solving Linear Equations
(ax + b = 0)

**4.15** Solving Quadratic Equations
(ax² + bx + c = 0)

**4.16** Trigonometric Functions
(cos, sin, tg, ctg)

**4.17** Conversion Between Degrees and Radians
(a° = b (rad))

**4.18** Absolute Value, Integer Part, Fractional Part of a Number
(|a|, [a], {a})

**4.19** Graph Plotting
(Line, parabola, hyperbola, sine wave, cosine wave, tangent function, cotangent function, circle, |x|, |y|, |x| and |y|, heart)

• **What may be added in the future:**

**4.20** Solving n-th Degree Equations

**4.21** Solving Parameters

**4.22** Solving Trigonometric Equations

**4.23** Representation of Irrational Numbers as Fractions (If possible)

**4.24** Derivatives and Integrals (Fundamentals of Mathematical Analysis)

### **5. User Guide.**

• Before using the application, it is important to understand how it works. First, you should familiarize yourself with the functions located in the left panel of the screen.

• After choosing, you need to click on the desired function and move to the right panel, where input fields will appear for entering numbers to perform the selected operation.

• To make it clearer what each input variable represents, there is a hint directly below the input fields in the form of a formula with the same variables set by the user.

• After entering the data, you need to perform the calculation by pressing the button below. After obtaining the result, you can choose a new function or clear the current calculations using the buttons in the bottom panel.

• If the selected operation is graph plotting, then after pressing the button below, a window with the required graph will appear, and the program itself will output the number 0 as the result.

• All calculations are saved in the history, which is available in the top right corner. It can be copied or cleared.

## **Part 2. Technical Document.**

### **1. Development Goals.**

• Create a convenient program that helps users solve various mathematical problems.

• Build a calculator with a wide range of functions from simple addition to graph plotting.

• Add visualization of mathematical functions to make them clear and intuitive.

• Create a visually appealing and clear interface in dark tones that is pleasant to use.

• Organize all functions into categories so users can quickly find the needed operation.

• Save calculation history so users can return to previous results.

### **2. Technologies Used.**

• **Programming Language:** Python

• **Libraries:** tkinter, math, json, os, typing, numpy, matplotlib

### **3. Project Architecture.**

• The project uses the **Model-View-Controller (MVC)** approach within a single main class Calculator.

• **Model (Model)** – these are mathematical functions such as addition, GCD calculation, and equation solving. They are implemented as class methods.

• **View (View)** – this is the entire graphical interface: buttons, input fields, and panels created using tkinter.

• **Controller (Controller)** – this is the logic that connects the interface and computations. It processes button clicks, data input, and result display.

### **4. Project Structure.**

• One main file calculator.py contains all the program code.

• The file calc_history.json is created automatically and stores the calculation history.

• The documentation folder contains the project description and instructions.

• The program includes one main class and more than 50 methods (functions) for various tasks.

• Each mathematical operation is implemented as a separate method, making the code clear and easy to modify.

### **5. Key System Components.**

• The interface manager creates all buttons, input fields, and panels visible to the user.

• The input system processes what the user types and can understand fractions and the number pi.

• The mathematical operations block contains more than 30 functions, from addition to solving equations.

• The graph module draws functions in a separate window with coordinate axes and labels.

• The history system stores recent calculations and displays them in a dedicated window.

### **6. User Interface Implementation.**

• The interface is designed in a dark color scheme with purple and turquoise accents.

• The left panel with buttons is divided into colored categories for easy navigation.

• The right panel changes depending on the selected operation – the required input fields appear.

• When hovering over a button, it changes color and displays the formula of the selected operation.

• Hotkeys are supported: Escape for reset, Ctrl+C for copying the result.

• The application window automatically opens centered on the screen at startup.

### **7. Development Process.**

• First, it was decided to use the Calculator v.1 code as a base.

• Then a mapping of operation names was added so that formulas appear when hovering over buttons.

• A function was implemented to display formulas when hovering the cursor over a button.

• New categories were added: FUNCTIONS and GRAPHS, and new operations were included in them.

• Functions for new operations (graph plotting) were implemented.

• Bugs were fixed and code cleanup was performed.

### **8. Main Challenges and Solutions.**

• **(1)** Challenge: It is necessary to understand what the input variables represent in each function.

Solution: When hovering over a function button, the formula for that operation is displayed.

• **(2)** Challenge: The graph grid has a limited size, so graphs that go beyond the boundaries cannot be seen.

Solution: The grid size was adjusted depending on the graph so that it is always visible.

• **(3)** Challenge: Some operations could not be seen because the panel has a fixed size, causing some functions to be outside the visible area.

Solution: A scrollbar was added to scroll through functions, and the mouse wheel can also be used.

### **9. Current Project Limitations.**

• Factorial cannot be calculated for numbers greater than 100 to prevent the program from freezing.

• Graphs cannot be zoomed in or out or moved with the mouse.

• The calculator does not support complex numbers, except for displaying equation roots.

• The history stores only the last 50 entries; searching or filtering is not available.

• In case of input errors, only a message is shown; incorrect fields are not highlighted.

• It is not possible to input full expressions consisting of multiple operations, only separate numbers for a specific selected operation.

### **10. Possible Improvements and Development Plans.**

• Split the code into multiple modules for easier maintenance.

• Add more advanced mathematical functions.

• Implement appearance settings: themes, colors, fonts.

• Improve the history system: add date and time, export to different formats, and search.

• Add support for multiple interface languages.

• Use multithreading so that heavy calculations do not block the interface.

• Create an executable .exe file to run the program without installing Python.
