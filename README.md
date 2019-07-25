# Robot Maze

The goal of the robot is move through a simple maze and stop when it detects the finish area (a black box). 
The robot is also required to use the same algorithm to solve different maze configurations. 
It is a two-wheeled differential drive robot with two sensors (a bumper sensor to detect the wall and a light sensor to
detect the floor color). To accomplish this, the robot will need a reference for its movement from one location to another. 
It will use the existing walls of the maze to guide itself to the finish line. The robot will use the obstacle (the walls) and 
it sensors to accomplish this task and will complete each maze within 5 minutes. This robot will be designed to follow the wall 
on the right side.

### Prerequisites

V-REP robot simulation platform is need to open the  and run the code - http://www.coppeliarobotics.com/

## Maze

![maze1](https://user-images.githubusercontent.com/9040355/38472913-0df0b6e4-3b55-11e8-9783-50b03177f109.png) 
![maze2](https://user-images.githubusercontent.com/9040355/38472918-2a78c1b2-3b55-11e8-8efa-20493a754194.png)
![maze3](https://user-images.githubusercontent.com/9040355/38472923-424ef590-3b55-11e8-9001-c8d4165ec6c0.png) 


## Description of code used and Algorithm

In establishing an algorithm, I first had to understand the steering system of a differential robot. The steering mechanism is as follows:
If both motors (wheels) turn at the same speed, the robot moves in a straight line.

If both motors (wheels) turn at the same speed, the robot moves in a straight line (see diagram below).
![screen shot 2018-04-08 at 5 16 33 pm](https://user-images.githubusercontent.com/9040355/38472680-a1781ed8-3b51-11e8-9452-f8814348a200.png)

 If one wheel rotates faster than the other, the robot follows a curved path
 inward toward the slower wheel (see diagram below).

![screen shot 2018-04-08 at 5 16 48 pm](https://user-images.githubusercontent.com/9040355/38472691-ce618ec0-3b51-11e8-95b4-ada67952f6ff.png)

## Running the tests

 As we can see, the steering of the robot has to do with the varying the speeds of
 the motor. A similar method is used to turn the robot when it is backing up. This
 fact is major part of the algorithm.
The Robot logic operates as follows:
- If the robot bumps into the wall, then backup (reverse, while slightly turning right)
- Then drive forward (with a slight right angle)


## Result

- Maze 1: http://youtu.be/F0u08FTDqjM
- Maze 2: http://youtu.be/Kzz3qOdEo0Y
- Maze 3: http://youtu.be/0e4cQ_B3c8I

## Authors

* **Kenny Whyte** 

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
