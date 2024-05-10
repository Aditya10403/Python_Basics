# **Inner Working**

![alt](https://miro.medium.com/max/1200/1*1athPfdP9St4mkB_hElM6g.png)

- ***When we run a Python script (.py file), the Python interpreter compiles the source code into bytecode instructions.***

- ***The Compiled Byte Code is a lower-level representation of the source code that the Python interpreter can understand and execute and is also Platform Independent***

- ***Byte code runs faster***

- ***`.pyc` - Compiled Python (frozen Binaries).After compilation, the bytecode is saved to a .pyc file. This file contains the precompiled bytecode instructions, which can be directly executed by the Python interpreter without the need for recompilation.***

- ***By using .pyc files, Python can execute scripts more efficiently because it doesn't have to recompile the source code every time the script is run. Instead, it can directly load and execute the precompiled bytecode from the .pyc file.***

- ***`__pycache__` - source change and python version***

- ***Works only for imported files***

- ***not for top level files (if in root directory)***


## Python Virtual Machine (PVM)

- *Code loop to iterate byte code*
- *Run time engine*
- *Also known as `Python Interpreter`*
- *`Interpretation`* - PVM interprets Python bytecode generated from source code.
- *`Platform Independence`* - PVM abstracts away platform-specific details, making Python code portable.
- *`Memory Management`* - handles memory allocation, deallocation, and garbage collection.
- *`Optimization`* - PVM may perform optimizations such as bytecode caching and just-in-time compilation (JIT) to improve performance.
- *`Standard Library Access`* - PVM provides access to the Python Standard Library, offering various modules for different functionalities.

### Byte Code is not machine code

- *Python specific interpretation*
- **Cypython (standard implementation), jython, Iron Python, Stackless, PyPy**