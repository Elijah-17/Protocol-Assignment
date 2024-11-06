# Protocol-Assignment
This is the code for a protocol assignment where I had to design my own protocol to transmit text characters between 2 Arduino's wirelessly. I used 2 Arduino Nano's and 7-bit leds with a clock led. These signals were received by photoresistors to determine high/low signals. 

### explanation
A text message can  be typed into the serial monitor on the transmitter, The serial monitor of the reciever displays the transmitted message.  
(explanation of how to use code)
_____
## Wiring
(wiring diagram)

## Transmitter Code
The transmitter code loops through the input string at [n] and sets currentLetter to be inputString[n]. Then currentLetter is checked to see if it is a letter or not. If it is a letter, the current letter is compared to see how far it is from the letter a. Shift is set to 1 if the letter is uppercase. The currentLetter now gets a number based on the distance from a. If the charecter is a digit, the value of the number is added to 64. This maps numbers starting at 64 so they are out of the way of letters and uppercase letters. This also sets the special charecter variable to 1. If the currentLetter is not any of those, it is compared to a bunch of cases, if any are true, the return value given a number. If it does not match anything it gets the number 0 and is assumed as a space. These numbers are then converted to binary and mapped to the LED's. There is a small delay to make sure all the led's have enough time to light up properly. Then the clock flashes high and low. Then [n] is increased by 1 to transmit the next charecter. Once all letters have been transmitted, all lights are turned on and the clock flashes once signaling the end of the string. 

## Reciever code
The receiver waits for the clock signal to go high, then it captures the state of all the other bit's. Once the state is captured, the character's binary number is converted into the base 10 number. If the special character light is on, the character number is passed into the special character decode function. This function takes the special character number and checks which case is met. The character that the case returns is added to the message output string. If the special light is not on the character number is passed into the letter decoding function. Here, the value of shift decides if the letter is uppercase or lowercase. Then the letters are mapped based on the distance from A or a. The letter is then added to the message output string. If all the lights are on, the reciever prints the recieved string to the console and the string clears. 
