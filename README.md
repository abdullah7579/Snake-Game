# Object-Oriented C++ Snake Game

A structured, terminal-based implementation of the classic Snake Game developed in C++ using clean Object-Oriented Programming (OOP) paradigms. The application features independent difficulty scaling, heap-allocated dynamic coordinate tracking arrays, persistent file streams for scoring, and custom ANSI-colored console manipulation to deliver an interactive retro-gaming experience directly in the terminal environment.

## Core Architecture & Requirements Breakdown
**Object-Oriented Design:** Encapsulates core game states, runtime rules, and state flags into a monolithic `data` class.Strict data encapsulation is maintained via private member variables exposed exclusively through public getter and setter interfaces.
**Dynamic Memory Management:** Utilizes heap-allocated dynamic integer arrays (`body_x` and `body_y`) to continuously log growing snake body positions. Memory handles are safely deallocated using the `delete []` operator at termination to guarantee zero memory leaks.
**Persistent File I/O Streams:** Integrates the `<fstream>` library to securely open, parse, and write to a persistent text-file scoring array. Features error-handling matrices to catch missing file configurations gracefully.
**Asynchronous Input Handling:** Implements non-blocking keyboard capturing via `<conio.h>` to drive rapid runtime vectors (`input()` and `control()`) without bottlenecking the main game loop thread.
**Console Manipulation & Rendering:** Utilizes low-level cursor hiding mechanisms (`console_set_handler()`), screen-refresh sequences (`system("cls")`), and embedded ANSI escape codes to render highly responsive, colored game-board boundaries, active targets, and obstacles.
**Algorithmic Randomization:** Employs synchronized time-seeded randomization (`srand(time(NULL))` and `rand()`) to auto-generate food nodes across the coordinate matrix. Includes algorithmic checks to prevent food nodes from spawning directly onto the snake's active coordinate layers.

## Feature to Coding Implementation Matrix
The codebase is segmented into key functional segments mapping technical design concepts to discrete software routines:

**Object-Oriented Setup:** Implements clean OOP principles, encapsulation, and constructors utilizing the `data()`, `snake_movement()`, and `game_over()` routines.
**File Architecture:** Manages data streams and file handling exceptions to read or log player performance metrics via `check_high_scores()`.
**Dynamic Memory Allocation:** Efficiently tracks changing heap parameters using dynamic array coordinates within the class constructor and destructor segments.
**Game Mechanics & Flow:** Drives underlying state logic and coordinate routing paths through the `control()` and `rigid_boundry_fun()` structures.
**User Input & Speed Scaling:** Processes non-blocking asynchronous keyboard tracking and variable runtime delays using `input()` and `set_level()`.
**Randomization & Visual Feedback:** Implements random number generation and precise ANSI color formatting strings using `srand_fun()` and `srand_check()`.
