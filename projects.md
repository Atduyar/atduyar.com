# Projects

## Minesweeper
Terminal-based puzzle game implemented across three languages (C#, Python, JavaScript), demonstrating language-specific approaches to game logic, algorithm implementation, and cross-platform terminal compatibility with ANSI escape sequences.

- **C#:** Object-oriented design with Cell, Board, StartScreen classes using System.Console
- **Python:** Procedural style with blessed library for terminal UI and list comprehensions
- **JavaScript:** Multi-paradigm approach with blessed Node.js library and event-driven architecture
- **Features:** Difficulty selection (Easy, Medium, Hard), custom board configurations, flagging system, flood-fill algorithm for revealing connected empty cells
- **GitHub:** [github.com/Atduyar/Minesweeper](https://github.com/Atduyar/Minesweeper)
- **Stars:** 4

## PingPongFasm
Assembly-C integration with neural network AI, implementing proper System V ABI calling conventions, stack alignment, and memory management coordination between FASM2 x86-64 assembly and raylib graphics.

- **Assembly:** FASM2 for game loop, rendering, collision detection, scoring system
- **C:** Neural network execution, audio playback, AI decision-making with feed-forward network
- **Integration:** Static linking with raylib, ELF64 binary format, 16-byte stack alignment before C function calls
- **Neural Network:** Single-layer architecture (4 inputs → 1 output) with sigmoid activation, weights set for paddle-y/ball-y comparison
- **GitHub:** [github.com/Atduyar/PingPongFasm](https://github.com/Atduyar/PingPongFasm)
- **Stars:** 3

## REKV
Multi-threaded in-memory key-value store with thread-safe hash map synchronization, published on crates.io as installable package featuring complete CRUD operations and concurrent access patterns.

- **Language:** Rust (edition 2021) with Arc<Mutex<HashMap>> for thread safety
- **Operations:** GET (retrieve value), SET (store value), DEL (delete key), ADD (increment numeric value)
- **Architecture:** Server mode on configurable address (127.0.0.1:4242), interactive CLI for testing, thread-per-connection model
- **Error Handling:** Result types for explicit success/failure paths, graceful handling of missing keys, type validation for ADD operations
- **GitHub:** [github.com/Atduyar/rekv](https://github.com/Atduyar/rekv)
- **Published:** crates.io

## Make2Game
Experimental 2D game engine with OpenGL batch rendering, SDL2 window management, Lua 5.4 scripting via C API, and Dear ImGui editor tools with live code editing capabilities.

- **Rendering:** OpenGL 3.3 Core Profile, GLEW extension loading, batch renderer supporting 10,000 quads per draw call, custom shader system with single-file parser
- **Scripting:** Lua 5.4 integrated via raw C API, custom bindings (textureAtlases, app), script lifecycle (Update/Render/Input hooks)
- **Editor:** Dear ImGui with dockable interface, ImGuiColorTextEdit code editor widget, texture atlas viewer, layer manager, log console with OpenGL error tracking
- **World System:** Custom text-based file format, layer organization with block-to-position mapping, texture atlases with sub-texture UV coordinate calculation
- **GitHub:** [github.com/Atduyar/Make2Game](https://github.com/Atduyar/Make2Game)
- **Stars:** 2

## LinkListBrainfuck
Doubly-linked list Brainfuck interpreter with dynamic memory tape, file-based loop navigation, ANSI terminal visualization, demonstrating first linked list implementation and recursive list traversal algorithms.

- **Data Structure:** Doubly-linked list with next/prev pointers, dynamic bidirectional growth on-demand
- **Memory:** Lazy allocation on pointer movement, 24 bytes per node overhead vs. 1 byte for arrays, manual cleanup via getFirstNode() traversal
- **Loop Implementation:** File-position based navigation with fseek/getc, O(n) loop rewind distance vs. O(1) with jump table (chose simplicity for first project)
- **Display:** Complex ANSI escape sequences (cursor positioning, color coding for root/current/executing nodes), real-time memory tape visualization
- **Brainfuck Commands:** All 8 implemented (`>`, `<`, `+`, `-`, `.`, `,`, `[`, `]`) with 8-bit wraparound for value operations
- **GitHub:** [github.com/Atduyar/LinkListBrainfuck](https://github.com/Atduyar/LinkListBrainfuck)
- **Stars:** 2

## NeuroevolutionFlappyBird
Genetic algorithm neural network visualization training 200 Flappy Bird agents, implementing feed-forward networks, fitness-based selection, crossover operators, and real-time training visualization in Octave.

- **Neural Network:** Fully connected multi-layer perceptron with configurable architecture, sigmoid activation function, forward propagation through all layers
- **Bird Agent:** State (position, velocity, alive status), brain (NeuralNetwork instance), 4 input features (distance to pipe, gap height, velocity, position), 1 output (jump decision threshold at 0.5)
- **Genetic Algorithm:** Population of 200 birds, fitness function (score + proximity bonus), selection process (top 20% performers), crossover (random weight mixing), mutation (random adjustments with adaptive rate), elitism (keep top 5 unchanged)
- **Visualization:** Real-time rendering at ~60 FPS, all birds translucent (overlapping density visualization), best bird highlighted, fitness score display, generation counter
- **GitHub:** [github.com/Atduyar/NeuroevolutionFlappyBird](https://github.com/Atduyar/NeuroevolutionFlappyBird)
- **Stars:** 1

## Evrenomi
Turkish social media blogging platform with mobile-responsive design, RESTful API architecture, user authentication, comment systems, and achieving 95+ Lighthouse performance scores.

- **Frontend:** Vanilla JavaScript (ES6+), semantic HTML5 markup, CSS3 (flexbox/grid, media queries), Fetch API for AJAX, manual state management with localStorage/session tokens
- **Backend:** RESTful API endpoints, user authentication (JWT or session-based), CRUD operations for posts and comments, SQL database integration, server-side rendering or JSON API
- **Features:** User interface for blog viewing, post listing with pagination, individual post pages, comment submission and display, user authentication UI (login/register), admin dashboard
- **Performance:** 95+ Lighthouse scores, mobile-responsive design with percentage-based layouts, cross-browser compatibility
- **GitHub:** [github.com/Atduyar/Evrenomi-frontend](https://github.com/Atduyar/Evrenomi-frontend)
- **Stars:** 1 (frontend) + 1 (backend) = 2

---

## Summary

### Total GitHub Stars: 16 across 8 projects

### Languages Used:
- **Systems:** Rust, C, C++, Assembly (FASM2, x86-64)
- **Web/Scripting:** C#, Python, JavaScript, TypeScript, Lua
- **Data Science:** Octave/MATLAB

### Domains:
- Game Development (4): Minesweeper, PingPongFasm, Make2Game, NeuroevolutionFlappyBird
- System Programming (3): REKV, LinkListBrainfuck, PingPongFasm
- Web Development (3): atduyar.com, Evrenomi-frontend, Evrenomi backend
- Machine Learning (1): NeuroevolutionFlappyBird
- Engine Development (1): Make2Game

### Key Achievements:
- Published package on crates.io (REKV)
- Multi-language implementation comparison (Minesweeper in C#, Python, JavaScript)
- Assembly-C neural network integration (PingPongFasm)
- Complete game engine architecture (Make2Game)
- Genetic algorithm implementation with visualization (NeuroevolutionFlappyBird)
- Full-stack blog platform (Evrenomi)
