# UCE (Unified Code Executor)

UCE is a light weight CLI tool that executes source files using command interface
<pre>
UCE
├── build                   // Compiler Output
├── include                 // Shared Headers
│   ├── command.h
│   └── dispatcher.h
├── Makefile
├── README.md
└── src                     // All Logic
    ├── commands
    │   └── run.c           // D
    ├── dispatcher.c
    ├── main.c              // Entry Point
    └── utils
        ├── file_utils.c
        └── string_utils.c
</pre>
How Pieces Connect

uce run main.c
main.c
--> reads "run"
dispatcher.c
--> matches "run"
run.c
--> handles execution logic
file_utils.c
--> checks file type
system runs command:
gcc main.c -o out && ./out
