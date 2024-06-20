# Sample codes for the class "Art of Simulation"

* Author: Akira Kageyama (kage@port.kobe-u.ac.jp)
* For Summer School 2024, Kobe Univ., Japan
* Language Used: [p5.js](https://p5js.org)
* Two Sample Codes (two directories)
    * `a_ball_bounce_on_parabola_multi`
        * One particle free-falls under gravity and bounces on the lower parabola.
    * `two_balls_on_parabolas_multi`
        * Two particles (with the same mass) slide without friction on separate parabolas.

* The basic structure of both programs is the same.
    - Solve the equations of motion with the `equation_of_motion()` function.
       - The system has 2 degrees of freedom.
       - Uses 4-component generalized coordinates (`GeneralCoords`).
    - Classical 4th-order Runge-Kutta method is used for numerical integration.
    - Coordinates and physical quantities are calculated as `float` (single precision) floating-point numbers.
    - The total energy is calculated and displayed to check accuracy.
  
* Visualization
    - The Preview window is divided into three areas.
 
``` 
        +------------+------------+------------+
        |            |            |            |
        |     x-y    |    x1-x2   |   x1-v1    |
        |     plot   |     plot   |  Poincare  |
        |(real space)|(Every time |    map     |
        |            |      steps)| (For v2=0) |
        |            |            |            |
        +------------+------------+------------+
```
       
  * Usage
    - Initial conditions can be changed in the `setup()` function.
    - Press the `u` key on the keyboard to accelerate the calculation (display).
    - Press the `d` key on the keyboard to decelerate the calculation (display).
    - Press the `s` key on the keyboard to pause (stop) and restart (start) the calculation (display).
    - Mouse click also toggles start/stop. 
    
  * Development History
    - Akira Kageyama (kage@port.kobe-u.ac.jp)
    - July 06, 2023: Developed in Processing
    - July 08, 2023: Converted into p5.js
    - June 20, 2024: Refactoring.
