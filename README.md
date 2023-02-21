# TurtleCrossing

This is a code for a Turtle Crossing game where the player needs to cross a busy street without getting hit by cars. Here is a breakdown of what each line does:

import time: imports the time module for time-related functions.
from turtle import Screen: imports the Screen class from the turtle module for creating the game screen.
from player import Player: imports the Player class from the player module for creating the player object.
from car_manager import CarManager: imports the CarManager class from the car_manager module for managing the cars.
from scoreboard import Scoreboard: imports the Scoreboard class from the scoreboard module for keeping track of the score.
screen = Screen(): creates a screen object.
screen.setup(width=600, height=600): sets the dimensions of the screen.
screen.tracer(0): turns off the screen updates.
player = Player(): creates a player object.
car_manager = CarManager(): creates a car manager object.
scoreboard = Scoreboard(): creates a scoreboard object.
screen.listen(): listens for key events.
screen.onkey(player.go_up, "Up"): when the "Up" arrow key is pressed, the player object's "go_up" method is called.
game_is_on = True: sets the game loop condition.
while game_is_on:: starts the game loop.
time.sleep(0.1): pauses the game for 0.1 seconds.
screen.update(): updates the screen.
car_manager.create_car(): creates a new car object.
car_manager.move_cars(): moves all the cars on the screen.
for car in car_manager.all_cars:: loops through all the car objects.
if car.distance(player) < 20:: checks if the player object collides with any car object.
game_is_on = False: stops the game loop.
scoreboard.game_over(): displays the "Game Over" message.
if player.is_at_finish_line():: checks if the player object reaches the finish line.
player.go_to_start(): moves the player object back to the starting position.
car_manager.level_up(): increases the speed of the cars.
scoreboard.increase_level(): increases the game level.
screen.exitonclick(): closes the game screen when the player clicks on it.
