# Automate-Boring-Stuff-with-Bash

Welcome to the repository dedicated to PC automation through Bash scripts! This repository has been created with the goal of streamlining and optimizing various activities on your machine using Bash scripts.

## Available Scripts

### 1. Operation through Command-Line Arguments

The `command_line_names.sh`  processes command-line arguments in the format of key-value pairs and performs a specific operation based on the provided keys. Here's the breakdown of what the script does:

- The script begins with a shebang line (**#!/bin/bash**) to indicate that it should be interpreted using the Bash shell.

- The for loop iterates over each argument passed to the script.

- Within the loop, index and val are extracted from each argument using the cut command with **-f1** and **-f2** options, respectively. This separates the argument into the key and value parts based on the **=** character.

- The **case** statement checks the value of **index** (the extracted key) and performs different actions based on its value:
  - If **index** is "X", the corresponding value is assigned to the variable **x**.
  - If **index** is "Y", the corresponding value is assigned to the variable **y**.

- After processing all the arguments, the **((result=x+y))** line calculates the sum of the values stored in the **x** and **y** variables.

- Finally, the script prints a message indicating the sum of **X** and **Y** with the calculated result using the **echo** command.

In summary, this script expects command-line arguments in the format of **key=value** pairs, where the keys are "X" and "Y" and the values are numeric. It extracts the values associated with "X" and "Y", calculates their sum, and prints the result in the form of "X+Y=result". If other keys are encountered, they are ignored.

### 2. Conky startup script during system boot

The `start_conky.sh` script is used to start the Conky application during system boot. Conky is a free, light-weight system monitor for X, that displays any information on your desktop. It is highly configurable and is able to monitor many system variables including the status of the CPU, memory, swap space, disk storage, temperatures, processes, network interfaces, battery power, system messages, e-mail inboxes, Arch Linux updates, many popular music players, and much more. Conky is licensed under the GPL and runs on Linux and BSD.
The script performs the following actions:
- The script includes a comment that indicates its purpose, which is to add Conky to your desktop during startup after waiting for 5 seconds.
- The shebang line (**#!/bin/bash**) at the beginning of the script indicates that it should be interpreted using the Bash shell.
- The **sleep 5** command introduces a delay of 5 seconds before proceeding to the next command. This allows time for the desktop environment to fully initialize before running the Conky application.
- The **conky** command is executed after the sleep period.

In summary, this script is designed to ensure that Conky, a system monitoring tool, is added to your desktop during system startup. It waits for 5 seconds to allow the system to stabilize and then launches the Conky application.
## How to Use the Scripts

1. Make sure you have execution permissions for the desired scripts. If not, run the following command to grant permissions:

   ```
   chmod +x script_name.sh
   ```

2. Run a script using the command:

   ```
   ./script_name.sh
   ```

3. Follow the instructions displayed in the command-line interface.

## License

These scripts are distributed under the MIT License. Feel free to use, modify, and share the scripts as you prefer.

---

I hope these Bash scripts are helpful in automating and simplifying your PC's daily tasks. If you have suggestions, improvements, or new scripts to share, don't hesitate to contribute to this repository or contact me!

Author: _**Pier Luca Anania**_