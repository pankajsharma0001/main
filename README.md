# Game Package with Raylib

Welcome to the Game Package repository! This project contains a collection of games developed using the Raylib library in C++. The first game included is Ping Pong, Tetris, 2048 and more games will be added in the future.

## Table of Contents
- [Introduction](#introduction)
- [Games Included](#games-included)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project is a game package developed using the [Raylib](https://www.raylib.com/) library in C++. Raylib is a simple and easy-to-use library to enjoy videogames programming. It allows you to create visually appealing games with minimal effort.

## Games Included

### 1. Ping Pong
A classic Ping Pong game where two players control paddles to hit the ball back and forth. The game continues until one player scores the winning point.

### 2. Tetris
A classic game where player have to complete a row of tile from seven unique blocks and prevent the block to reach the top of screen.

### 3. 2048
A classic game where player have to slide the tiles a two tile with same value merge to form double of that tile. The game is over when you reach out of move or
completes 2048.

## Installation

To run the games in this repository, you need to have Raylib installed on your system. Follow the steps below to set up your environment:

## Installation

1. **Install Dependencies**:

   Ensure you have installed all necessary dependencies for your platform. For detailed instructions, refer to the Raylib documentation.

2. **Update System Environment Variables**:

   Add the following path to your system environment variables:
   ```bash
   C:\raylib\w64devkit\bin

3. **Navigate to Source Directory**:

   Open a terminal and navigate to the following path:
   ```bash
   C:\raylib\raylib\src

4. **Compile Raylib**:

   In the terminal, run the following command:
   ```bash
   mingw32-make PLATFORM=PLATFORM_DESKTOP

5. **Locate Compiled Library**:

   After the command executes successfully, a new file named ```libraylib.a``` will be created.

6. **Replace Existing Library**:

   Copy the newly created libraylib.a file and replace the existing ```libraylib.a``` file in the lib folder within your project directory.

7. **Create Makefile**:

   Create a Makefile in your project directory and add the following content:
   ```bash
   # Define the source files for the project
   SOURCES = ./src/main.cpp

   # Default target to compile the project
   default:
	g++ $(SOURCES) -o ./build/game.exe -g -O1 -Wall -Wno-missing-braces -I include/ -L lib/ -lraylib -lopengl32 -lgdi32 -lwinmm 
    
   # Run the compiled executable
   ./build/game.exe


8. **Run the Program**:

   To compile and run the program, execute the following command in the terminal:
   ```bash
   make


## Usage

After building the project, you can run the game using the command mentioned above.  
Use the following controls to play   
**1. Ping Pong:**

- **Single Player Controls:**
  - `W` - Move paddle up
  - `S` - Move paddle down
  - `Space` - Pause the game

- **Double Player Controls:**
  - `W` - Move left paddle up
  - `S` - Move left paddle down
  - `Up Arrow` - Move right paddle up
  - `Down Arrow` - Move right paddle down
  - `Space` - Pause the game

**2. Tetris**

  - `Left Arrow` - Move block left
  - `Right Arrow` - Move block right
  - `Up Arrow` - Rotate block
  - `Down Arrow` - Move block down quickly
  - `Right Shift` - Directly place the block at the bottom
  - `Space` - Pause

**3. 2048**

  - `Left Arrow` - Slide block left
  - `Right Arrow` - Slide block right
  - `Up Arrow` - Slide block up
  - `Down Arrow` - Slide block down

## Contributing

Contributions are welcome! If you have ideas for new games or improvements to the existing ones, please feel free to fork this repository, make your changes, and submit a pull request. Here are the steps to contribute:

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
