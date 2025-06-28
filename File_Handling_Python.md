
# ✅ 1. Common Methods Used in File Handling

| Method         | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `open()`       | Opens a file and returns a file object.                                     |
| `read()`       | Reads the entire content of the file.                                       |
| `readline()`   | Reads one line from the file.                                               |
| `readlines()`  | Returns a list containing all lines in the file.                            |
| `write()`      | Writes content to the file. (Overwrites existing content in write mode.)    |
| `writelines()` | Writes a list of strings to the file.                                       |
| `close()`      | Closes the file. It's important to free up system resources.                |
| `seek()`       | Changes the file pointer position. Useful for reading from a specific position. |
| `tell()`       | Returns the current file pointer position.                                  |
| `with` statement | Automatically closes the file when done (Context Manager).                |

# ✅ 2. File Opening Modes in Python

| Mode   | Meaning                              | Use Case                                              |
|--------|--------------------------------------|-------------------------------------------------------|
| `'r'`  | Read (default). File must exist.     | Reading contents from a file.                         |
| `'w'`  | Write. Overwrites the file if it exists. | Writing new content to file (destructive).        |
| `'a'`  | Append. Adds content to the end of file. | Adding new data to existing file.                  |
| `'x'`  | Exclusive creation. Fails if file exists. | Creating a new file only if it doesn't exist.     |
| `'r+'` | Read and write. File must exist.     | Read and modify content without truncating.          |
| `'w+'` | Write and read. Truncates file.      | Overwrite and then read back.                        |
| `'a+'` | Append and read.                     | Add new data, also allows reading.                   |
| `'b'`  | Binary mode.                         | For binary files like images, PDFs, etc.             |
| `'t'`  | Text mode (default).                 | For text files.                                      |
