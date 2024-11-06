# Protocol-Assignment
This is the code for a protocol assignment where I had to design my own protocol to transmit text characters between 2 Arduino's wirelessly. I used 2 Arduino Nano's and 7-bit leds with a clock led. These signals were received by photoresistors to determine high/low signals. 

### explanation
_____
## Wiring


## Reciever code
The receiver waits for the clock signal to go high, then it captures the state of all the other bit's. Once the state is captured, the charecter's binary number is converted into the base 10 number. If the special charecter light is on, the charecter number is passed into the special charecter decode function. This function takes the special charecter number ans sees which case is met. The carecter that the case returns is added to the message output string. If the special light is not on the charecters number is passed into the letter decoding function. Here, 

