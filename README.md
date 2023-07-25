# File-_Management_using_c


This C code is a simple file manipulation program that performs various file-related operations. The program takes command-line arguments to execute different functionalities. Here's a brief description of each function:

1. create_file: This function is used to create a new file with the specified path and permissions. If a file already exists with the same path, it will be replaced with the new file. The file permissions are provided as an octal string, which is converted to an integer using sscanf.

2.read_file: This function reads a specified number of bytes (nbytes) from a file, starting from a particular offset (offset). It opens the file in read-only mode, sets the offset, reads the data into a buffer, and then prints the read data to the console.

3.write_file: This function reads a specified number of bytes (nbytes) from the standard input (stdin) and writes them to a file at a particular offset (offset). The source data is read from the standard input and then written to the file specified by path1. The file is opened in write-only mode with the O_CREAT flag to create a new file if it does not exist.

4.display_info: This function displays statistical information about a file specified by its path. It uses the stat function from sys/stat.h to fetch details like file size, number of links, file inode, and file permissions. The file permissions are displayed as a combination of characters ('d', '-', 'r', 'w', 'x').

5.copy_file: This function copies the content of a source file (src_path) to a destination file (dst_path). If the destination file exists, it overwrites its content. If the destination file does not exist, it creates a new file with read, write, and execute permissions for the user, group, and others.

In the main function, the program checks the number of command-line arguments to determine which operation to perform. It calls the corresponding function with the appropriate arguments based on the input provided through the command line.

Overall, this program demonstrates basic file handling operations in C, such as creating, reading, writing, and copying files, as well as displaying file information.
