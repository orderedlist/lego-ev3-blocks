# Lego Mindstorm EV3 MyBlocks

These blocks and programs were developed by the Elm Road Elementary Robotics team in Mishawaka, Indiana. Our team decided that it would be best to let other teams use, and improve upon, these blocks in an effort to promote cooperation.

## [Calibrate Gyro](https://github.com/orderedlist/lego-ev3-blocks/blob/master/calibrate-gyro.ev3s)

This block is used at the beginning of a program to recalibrate the gyro sensor to reduce drift. Our team learned that by switching the type of reading from the sensor (eg. from angle to rate), the sensor automatically calibrates. There is a brief (0.4s) waiting period to let the robot come to rest from being moved and pressing buttons, after which it switches to measuring rate, then to angle. Another brief waiting period (0.1s) ensures the sensor is ready to be read.

## [Calibrate Reflector](https://github.com/orderedlist/lego-ev3-blocks/blob/master/calibrate-reflector.ev3s)

This program is used to calibrate the color sensor's reflected light meter. Simply run this program, and follow the prompts on the EV3 screen. Place the sensor on the appropriate color on the board, and press the button.

## [Gyro Drive](https://github.com/orderedlist/lego-ev3-blocks/blob/master/gyro-drive.ev3s)

This MyBlock uses the gyro sensor to drive forward for a specified number of rotations at a specified power. The block uses simple algebra to adjust the motor speeds to keep the robot pointing at the originally measured angle, ensuring the robot drives straight.

## [Line Follow](https://github.com/orderedlist/lego-ev3-blocks/blob/master/line-follow.ev3s)

This MyBlock uses the color sensor to measure reflected light so as to stay halfway (measuring 50) between  the black and white lines that appear on mission boards. Simple algebra is used to adjust the motors more drastically based on how close to 0 or 100 the sensor shows. This block will follow a line for a specified number of seconds.

## [Turn Degrees](https://github.com/orderedlist/lego-ev3-blocks/blob/master/turn-degrees.ev3s)

This MyBlock is used to turn the robot toward a specified degree on the mission board, based on the originally measured orientation at the beginning of the mission (using the calibrate-gyro block). It does so by turning the motors, and slowing down the closer to the desired angle it reads, so it can stop more accurately.

This program does not reset the gyro measurement so as not to get further and further off the more turns you make. This block assumes that setting a degree less than the current will turn left, greater will turn right.

For example, if the robot is facing north, and you want it to face east, simply set TurnDegrees to 90. To face north again, set to 0. To face west, set to -90.
