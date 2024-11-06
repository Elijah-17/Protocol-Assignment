# Protocol-Assignment
This is the code for a protocol assignment where I had to design my own protocol to transmit text characters between 2 Arduino's wirelessly. I used 2 Arduino Nano's and 7-bit leds with a clock led. These signals were received by photoresistors to determine high/low signals. 

### explanation
A text message can  be typed into the serial monitor on the transmitter 
(explanation of how to use code)
_____
## Wiring
(wiring diagram)

## Transmitter Code
The transmitter code checks 

## Reciever code
The receiver waits for the clock signal to go high, then it captures the state of all the other bit's. Once the state is captured, the character's binary number is converted into the base 10 number. If the special character light is on, the character number is passed into the special character decode function. This function takes the special character number and checks which case is met. The character that the case returns is added to the message output string. If the special light is not on the character number is passed into the letter decoding function. Here, the value of shift decides if the letter is uppercase or lowercase. Then the letters are mapped based on the distance from A or a. The letter is then added to the message output string. 
