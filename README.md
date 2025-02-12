<a href="https://www.cprogramming.com"><img src="https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white" height="25em" alt="C"/></a>

# Get_Next_Line

## Goal

Write a function that reads a line from a file descriptor, returning it as a string. The function should handle multiple file descriptors and different buffer sizes efficiently, allowing users to read files line by line.

## Key Features

- Line Reading: Reads one line at a time from a file descriptor.
- Multiple File Descriptors: Works with multiple file descriptors simultaneously without losing context.
- Dynamic Buffer Size: Adapts to different buffer sizes provided by the user.
- Memory Management: Ensures proper allocation and freeing of memory to avoid leaks.

## Implementation Details

- Static Variable: Uses a static variable to store leftover data between function calls, enabling continuity across reads.
- Buffer Management: Reads data into a buffer and extracts lines, saving any remaining data for the next call.
- Edge Cases: Handles cases like end-of-file, empty lines, and invalid file descriptors.

## Challenges

- Memory Management: Avoiding leaks and ensuring efficient memory usage.
- Buffer Size: Handling different buffer sizes without losing data or performance.
- Multiple Calls: Maintaining state between function calls for the same file descriptor.

## Skills Developed

- File I/O: Learning to interact with file descriptors and read data in chunks.
- Memory Handling: Managing dynamic memory allocation and freeing.
- Edge Case Handling: Addressing various scenarios like EOF, empty lines, and invalid inputs.

## Installation

1. Clone the repository:
```sh
git clone git@github.com:casomarr/42-Get_Next_Line.git
```

2. Navigate to the project directory:
```sh
cd get_next_line  
```

3. Compile the program with the get_next_line files:
```sh
gcc -Wall -Wextra -Werror -D BUFFER_SIZE=<size> get_next_line.c get_next_line_utils.c main.c -o gnl  
Replace <size> with the desired buffer size (e.g., 42).
```

4. Run the program with a test file:
```sh
./gnl < test_file.txt  
```

5. Repeat the same process for the bonus part
