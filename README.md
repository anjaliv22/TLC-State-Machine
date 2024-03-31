Alongside my partner, Mahi Joshi, I have created this fully functional project that operates on a Logical Step Board.
This project involved programming a traffic signal that operates at ann intersection with North-South lights and East-West lights in VHDL. The purpose of this project is to use the behaviour
of a Moore machine to create a traffic signal that runs for a total of 16 states, each state being controlled by numerous variables. 
-
Parts of the Logical Step Board that are used on the Logical Step Board:
- Led 0,1,2,3,4,5,6,7
- Push buttons 0 and 1
- Seven Segment Digit 1 and Digit 2 ( 2 seven segment displays)

Functionality of the Step Board:
- There are 2 seven segment displays being used, the first display is used as a traffic signal for the East-West direction. The second display is used as a traffic signal in the North-South direction.
- Segements A,D,G are used where A = RED, D = Green or Flashing Green, and G = AMBER
- Red: lasts for 8 states
- Amber: lasts for 2 states
- Green: lasts for 4 states
- Flashing green: lasts for 2 states
On the logical step board the user is given 2 inputs:
- Push button [0]: By pressing this the user is making a request to cross in the North-South direction. Once the request is made the signal is then shown on LED[1] (the second led on the step board)
- Push button [1]: By pressing this the user is making a request to cross in the East-West direction. Once the request is made the signal is then shown on LED[3] (the fourth led on the step board)

Led[0]: this led is used as a crossing display in the North-South direction, when it turns on it is letting the pedestrian know that it is now safe to cross as the light is solid green in the desired direction. 
Led[2]: this led is used as a crossing display in the East-West direction, when it turns on it is letting the pedestrian know that it is now safe to cross as the light is solid green in the desired direction. 
Leds [7->4]: these 4 leds displays the number of the current state of the traffic light signal (0 to 15) in binary. 

- If a pedestrian request is made in either NS or Ew direction at the first 2 states of the red light with no previous request made then the traffic signal is programmed to jump 6 states to make the wait shorter.
- If a previous request was made and a pedestrian is currently crossing then the traffic signal will not jump states and will continue as normal. 
