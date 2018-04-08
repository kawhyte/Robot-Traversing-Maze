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

| `Maze 1` | `Maze 2` | `Maze 3` |
| --- | --- | --- |
| ![maze1](https://user-images.githubusercontent.com/9040355/38472762-ed2889b6-3b52-11e8-85ad-debcfbfd5268.png) | 
!![maze2](https://user-images.githubusercontent.com/9040355/38472770-ff3d326e-3b52-11e8-938d-a3bc6256af79.png)| 
!![maze3](https://user-images.githubusercontent.com/9040355/38472777-16efc64c-3b53-11e8-9632-43a96b954a6c.png) |


## Description of code used and Algorithm

In establishing an algorithm, I first had to understand the steering system of a differential robot. The steering mechanism is as follows:
If both motors (wheels) turn at the same speed, the robot moves in a straight line.

If both motors (wheels) turn at the same speed, the robot moves in a straight line (see diagram below).
![screen shot 2018-04-08 at 5 16 33 pm](https://user-images.githubusercontent.com/9040355/38472680-a1781ed8-3b51-11e8-9452-f8814348a200.png)

 If one wheel rotates faster than the other, the robot follows a curved path
 inward toward the slower wheel (see diagram below).

[screen shot 2018-04-08 at 5 16 48 pm](https://user-images.githubusercontent.com/9040355/38472691-ce618ec0-3b51-11e8-95b4-ada67952f6ff.png)

## Running the tests

 As we can see, the steering of the robot has to do with the varying the speeds of
 the motor. A similar method is used to turn the robot when it is backing up. This
 fact is major part of the algorithm.
The Robot logic operates as follows:
- If the robot bumps into the wall, then backup (reverse, while slightly turning right)
- Then drive forward (with a slight right angle)

## Flow Chart

![screen shot 2018-04-08 at 5 26 41 pm](https://user-images.githubusercontent.com/9040355/38472720-1cc8d29e-3b52-11e8-96b3-fcbcac47612d.png)

## Block Diagram

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc