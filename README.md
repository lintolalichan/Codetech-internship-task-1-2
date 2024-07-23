Name: Linto Lalichan

company: CODTECH IT SOLUTIONS

ID: CT08DS3166

DOMAIN: CYBER SECURITY & ETHICAL HACKING

DURATION: JUNE 25,2024 to JULY 25,2024

MENTOR: Santhosh Kumar

overview of the project

PROJECT:Vulnerability scanning tool

Objective

This Python script creates a GUI application using the tkinter library. The application is a vulnerability scanning tool that allows users to scan a specified IP range for open ports and check for outdated software versions. Here's a detailed breakdown of each part of the code:

Imports and Setup:

tkinter and messagebox: Used for creating and managing the GUI components and displaying message boxes.

socket: Used for network communication to scan open ports.

os: Used to execute shell commands to check software versions.

threading: Used to run tasks in separate threads to avoid freezing the GUI.

Network Scanning Function (scan_network):

Purpose: Scans a specified IP range for open ports.

Process:Retrieves the IP range entered by the user.

Splits the range into starting and ending IP addresses.

Iterates over each IP address and port (from 1 to 65535) within the range.

Creates a socket and attempts to connect to each port. If the connection is successful (result = 0), the port is considered open and is added to the list.

Updates the GUI with the results of open ports.

Software Version Checking Function (check_software_versions):

Purpose: Checks for outdated software versions.

Process:Defines a list of software to check, along with their version commands. Executes each command and reads the output.

If the command output indicates that the software is not found or outdated, it is added to the list of outdated software. Updates the GUI with the results.

Button Click Handler (on_scan_button_click):

Purpose: Handles the event when the "Scan Network" button is clicked.

Process:Clears previous scan results.

Starts the network scanning and software version checking in separate threads to keep the GUI responsive.

GUI Setup:

Main Application Window:Creates the main application window with a title and specified size.

IP Range Input:Adds a label and an entry field for the user to input the IP range.

Scan Button:Adds a button that, when clicked, starts the scan.

Labels for Displaying Results:Adds labels that display the results of the port scan and software version check.

Main Application Loop:Runs the main loop to keep the GUI active and responsive.
