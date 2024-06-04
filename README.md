# Maze Game

This maze game was developed as part of the LCOM course, utilizing low-level C programming on the MINIX operating system. It offers both single-player and multiplayer modes, challenging players to navigate intricate labyrinths as quickly as possible.

## Table of Contents

1. [Introduction](#introduction)
2. [User Instructions](#user-instructions)
    - [Running the Project](#running-the-project)
    - [Menu](#menu)
    - [Controls](#controls)
    - [Singleplayer Mode](#singleplayer-mode)
    - [Multiplayer Mode](#multiplayer-mode)
    - [Screen with Instructions](#screen-with-instructions)
3. [Project Status](#project-status)
4. [Code Organization and Implementation](#code-organization-and-implementation)
    - [Data Structures](#data-structures)
    - [Game Logic](#game-logic)
    - [The Maze](#the-maze)
    - [Menu](#menu-1)
5. [Conclusion](#conclusion)
6. [License](#license)
7. [Contributing](#contributing)
8. [Group Members](#group-members)

## Introduction

This maze game was developed as part of the LCOM course, utilizing low-level C programming on the MINIX operating system. It offers both single-player and multiplayer modes, challenging players to navigate intricate labyrinths as quickly as possible. Designed to run on MINIX, this project provides valuable insights into operating system concepts and low-level programming.

![Maze Game Screenshot](images/maze_game_screenshot.png)

## User Instructions

### Running the Project

To run the project, the user just has to compile by running `make` in the source code folder (`proj/src`). Then, just run `lcom_run proj host`. If a second user wants to play in multiplayer with the first user, the run command must be `lcom_run proj client`.

### Menu

We developed a comprehensive and user-friendly menu for our game, featuring four distinct entries to enhance the player experience:
- **Singleplayer**: Singleplayer game where your goal is to reach the end as soon as possible.
- **Multiplayer**: Multiplayer game where you and another player will compete, and the one who finishes their labyrinth faster wins.
- **How to play**: Instructions on how to move and play the game.
- **Exit**: Exit the game.

The menu can be controlled using the mouse to select and click on each button.

![Game Menu](images/game_menu.png)

### Controls

The player can move in four directions: forward, backward, left, and right. Rotation is determined by a trigonometric relationship between the player's position and the mouse's position, enhancing the intuitive nature of the controls.

### Singleplayer Mode

In single-player mode, the player navigates through a simple labyrinth to reach the end in the shortest time possible. The player is surrounded by a small visible circle, allowing them to see a fraction of the environment. Movement and rotation are controlled using the mouse and keyboard, providing a smooth and intuitive experience. Once the player reaches the end of the labyrinth, the screen displays the elapsed time.

![Singleplayer Mode](images/singleplayer_mode.png)

### Multiplayer Mode

To make the game more fun and competitive, we developed a multiplayer mode. In this mode, two players compete to see who finishes the maze first. The labyrinths are randomized, so a player not only needs to be fast but also be lucky to get an easy maze.

### Screen with Instructions

Intended for new players, the "How to Play" screen provides instructions about the controls for the game.

![Instructions Screen](images/instructions_screen.png)

## Project Status

The project is complete and fully functional. It includes the following devices and functionalities:
- Timer
- Keyboard & Mouse
- Video Card
- Serial Port
- Real Time Clock

## Code Organization and Implementation

### Data Structures

- **Stack**: Used for the maze generation algorithm.
- **Linked List**: Used for an algorithm to solve the maze.
- **Queue**: Used for managing game states.

### Game Logic

- **Initialization**: Setting the initial position of the player and generating the maze.
- **Game Loop**: Updating the display for each frame.
- **Keyboard and Mouse Handling**: Processing inputs separately from the frame generation to ensure responsiveness.
- **Flashlight**: Restricting the player's view to a circle around them.
- **Multiplayer Implementation**: Using the serial port for communication between two computers.

### The Maze

- **Data Representation**: A grid of cells representing the maze.
- **Maze Generation**: Using a randomized iterative implementation of a depth-first search algorithm.
- **Algorithm to Solve the Maze**: Implementing Dijkstra’s Algorithm to calculate the optimal path.
- **Collision System**: Ensuring players cannot phase through walls.

### Menu

A collection of buttons with on-click actions, implemented with a black background, centered horizontally, and changing color when hovered.

## Conclusion

Overall, we are pleased with the final result. While it is a simple game, it effectively utilizes all the concepts taught in class in interesting ways. This project allowed us to solidify our knowledge of various concepts and provided a strong sense of accomplishment.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

We welcome contributions to enhance this project. Please read the [CONTRIBUTING](CONTRIBUTING.md) file for guidelines on how to get involved.

## Group Members

LCOM Project for group T13G01.

Group members:
- Henrique Fernandes (up202204988@up.pt)
- José Sousa (up202208817@up.pt)
- Luís Cordeiro (up202205425@up.pt)
- Miguel Cabral (up202204996@up.pt)

