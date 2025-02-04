# Qt-Based System Monitoring & Process Execution Application

## Overview
This project is a **Qt-based GUI application** designed for monitoring system performance (CPU and RAM usage) and executing external programs with specific arguments. The application integrates **QProcess** for process management and **QTimer** for real-time system updates.

## Features
- **Qt GUI Interface**: Provides a graphical user interface for user interaction.
- **System Monitoring**:
  - Displays real-time **CPU usage** by reading from `/proc/stat`.
  - Shows **RAM usage** using the `free -m` command.
- **Process Execution**:
  - Executes external programs with user-defined arguments.
  - Captures and displays program output in the UI.
- **Automatic Updates**:
  - Uses `QTimer` to refresh system stats every second.
  
## Prerequisites
Ensure you have the following dependencies installed:

### Required Software:
- Qt 5 or Qt 6 (with Qt Widgets module)
- CMake (version 3.5 or higher)
- A C++17 compatible compiler (GCC, Clang, MSVC)

### Installation Instructions:
#### Install Qt
```sh
sudo apt update
sudo apt install qtbase5-dev qtchooser qt5-qmake qtbase5-dev-tools
```

## Compilation and Execution

### Build the Project
```sh
mkdir build && cd build
cmake ..
make
```

### Run the Application
```sh
./untitled
```

## Code Structure
```
├── CMakeLists.txt           # CMake build configuration
├── main.cpp                 # Application entry point
├── mainwindow.cpp           # Main window logic
├── mainwindow.h             # Main window header file
├── mainwindow.ui            # UI file for Qt Designer
```

## Functionality
### System Monitoring
- Reads CPU usage from `/proc/stat`.
- Extracts and calculates CPU percentage.
- Reads RAM usage using the `free -m` command.
- Updates UI every second using `QTimer`.

### Process Execution
- Launches external programs using `QProcess::start()`.
- Passes integer arguments based on button clicks.
- Captures standard output and displays results.

## Possible Enhancements
- **Graphical Charts**: Visualize system resource usage over time.
- **Process Management**: Ability to terminate running processes.
- **Multi-Process Execution**: Run multiple commands simultaneously.
- **Cross-Platform Support**: Ensure compatibility across Windows, Linux, and macOS.

## Author
**Mahmoud Hany** - Computer Engineering Student & AI Enthusiast

## License
This project is licensed under the MIT License.

