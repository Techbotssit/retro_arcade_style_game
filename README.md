ESP32 Retro Arcade Game Console
Overview

This project is a retro-style embedded arcade game console built using an ESP32 microcontroller and a 128×64 SSD1306 OLED display.
It features a menu-driven interface that allows users to play multiple classic 2D arcade games using physical buttons and buzzer-based audio feedback.

The project demonstrates embedded system design, state-machine–based software architecture, real-time input handling, and graphics rendering on resource-constrained hardware.

Project Type

Embedded Systems Project

Retro Arcade Game System

Menu-Driven Multi-Game Console

Educational / Demonstration Platform

Games Supported

Snake (Cobra) – Grid-based movement and collision detection

Pong – Paddle-and-ball physics game

Shooter – Vertical shooter with bullets and enemies

Racer – Lane-based obstacle avoidance racing game

Tetris – Block-fall puzzle game with rotation and line clearing

Each game runs independently and can be exited back to the main menu.

Hardware Components

ESP32 development board

SSD1306 OLED display (128×64, SPI)

6 push buttons

Buzzer

USB power supply

Pin Configuration
OLED (SPI)
Signal	GPIO
CS	5
DC	4
RST	15
Buttons
Function	GPIO
UP	25
DOWN	26
LEFT	27
RIGHT	14
SELECT	32
OK / START	33
Buzzer
GPIO
13
Software Architecture

Menu-driven state machine

Central controller manages:

Start screen

Menu navigation

Game switching

Each game implemented as a separate module

Only one game active at a time

Each game module handles:

Game states

Input processing

Graphics rendering

Sound effects

Graphics and Display

OLED driven using U8g2 graphics library

Full-frame buffer rendering

Graphics drawn in RAM and sent to display in a single update

Ensures smooth, flicker-free animation

Input and Audio

Buttons configured using INPUT_PULLUP

Software debouncing applied

Buzzer used for:

Menu feedback

Gameplay sounds

Game over alerts

Memory Usage

Program stored in flash memory

Runtime data and graphics buffer stored in RAM

Approximate usage:

Flash: a few hundred kilobytes

RAM: ~40 KB

Source and Learning Approach

This project is adapted from an existing GitHub repository.
The focus was on understanding the system, integrating hardware, modifying functionality, and achieving stable execution rather than claiming originality.
