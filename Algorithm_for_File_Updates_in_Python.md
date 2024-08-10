[Original Document](https://docs.google.com/document/d/1XJg5XydTD8OyF6ORbcgp0IUHGO973HqfMIChr5rB4cw/edit?usp=sharing)
# Algorithm for File Updates in Python

# Algorithm for File Updates in Python

## Project Description

This project focuses on managing an IP address allow list stored in a text file called `allow_list.txt`. The goal was to update this file by removing specific IP addresses that are no longer authorized. Using Python, we read the file’s content, converted it into a list, and filtered out the IP addresses that matched those in a `remove_list`. The updated list was then converted back into a formatted string and saved, ensuring the file accurately reflects the current access permissions.

## Open the File That Contains the Allow List

To start the algorithm, I opened the file named `allow_list.txt`. Initially, I assigned this file name to the variable `import_file` as a string.

In my algorithm, the `with` statement is used in conjunction with the `.open()` function to open the allow list file in read mode. This setup allows for accessing the IP addresses stored in the file. The `with` keyword manages resource handling by ensuring the file is automatically closed once the block is completed. In the line `with open(import_file, "r") as file:`, the `open()` function takes two arguments: the first specifies the file to open, and the second, `"r"`, denotes that the file is to be read. The `as` keyword assigns the opened file to the variable `file`, which is used to interact with the file’s contents within the `with` block.

## Read the File Contents

The `open()` function opens the file `allow_list.txt` in read mode (`"r"`) and the `.read()` method reads the entire content of the file into the variable `ip_addresses`. Finally, the `print()` function is used to display the contents stored in `ip_addresses`. The `with` statement and `open()` function are key for file handling, while `print()` is used for output. Indentation is crucial to define the block of code under the `with` statement.

## Convert the String into a List

The `.split()` function is applied to a string variable to convert it into a list. This function works by splitting the contents of the string into individual elements based on whitespace by default. In this algorithm, `.split()` is used to transform the `ip_addresses` string, which contains IP addresses separated by whitespace, into a list of these addresses. This conversion facilitates the process of removing specific IP addresses from the allow list. The resulting list is then reassigned to the `ip_addresses` variable to reflect the updated format.

## Iterate Through the Remove List

To iterate through the `remove_list` and remove IP addresses from `ip_addresses`, we can use a `for` loop in Python. The `for` keyword initiates the loop, with `element` as the loop variable representing each IP address in `remove_list`. Inside the loop, we would use an `if` statement combined with the `in` keyword to check if `element` is in `ip_addresses` and then use the `remove()` method to delete it. This approach leverages the `for` keyword for iteration, `in` for membership testing, and `remove()` to modify the list.

## Remove IP Addresses That Are on the Remove List

To remove IP addresses from `ip_addresses` that are also in `remove_list`, use a `for` loop to iterate through each `element` in `remove_list`. Inside the loop, use an `if` statement with the `in` keyword to check if `element` exists in `ip_addresses`. If the condition is true, apply the `.remove()` method to `ip_addresses` to delete the `element`. This approach utilizes the `for` keyword for iteration, `if` and `in` for conditional membership testing, and `.remove()` to modify the list by removing the specified items.

## Update the File with the Revised List of IP Addresses

To update the file with the revised list of IP addresses, first convert the `ip_addresses` list into a string where each IP address is separated by a space using the `.join()` method with `" "` as the delimiter. This concatenates the list elements into a single string with spaces between them. Next, use a `with` statement to open the file specified by `import_file` in write mode (`"w"`). Within this `with` block, use the `.write()` method to overwrite the file’s contents with the updated string. This ensures the file is correctly updated, with `.join()` formatting the list and `.write()` handling the file update.

## Summary

The algorithm begins by reading the contents of a text file into a string using Python’s `open()` and `.read()` functions. It then splits the string into a list of IP addresses with `.split()`. The script iterates through this list, removing addresses found in a predefined `remove_list` using the `.remove()` method. After filtering, the list is converted back to a single string with each address separated by spaces using `.join()`. Finally, the file is rewritten with the updated list using `open()` in write mode and `.write()`. This process ensures the file is updated to reflect the most current list of allowed IP addresses.

---