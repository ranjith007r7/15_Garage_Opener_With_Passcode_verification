# 15_Garage_Opener_With_Passcode_verification
## Garage Opener with Passcode Verification

This Arduino project combines a garage door opener with a passcode verification system to enhance security. The system uses a stepper motor to control the garage door's movement and verifies a passcode entered via a keypad before allowing access.

### Components Used
- Arduino board
- Ultrasonic distance sensor (NewPing)
- Stepper motor (AccelStepper)
- 16x2 LCD display (with I2C interface)
- 4x4 keypad
- RGB LED
- Buzzer

### Description
1. **Initialization**: Upon startup, the system initializes all components and displays "Garage Door Opener" on the LCD.
2. **Passcode Entry**: The user is prompted to enter a passcode using the keypad. Only numeric keys are allowed. The passcode is entered by pressing '#' to submit.
3. **Passcode Verification**: If the correct passcode is entered, "Access Granted" is displayed on the LCD, the RGB LED glows blue, and the buzzer emits two beeps. If the passcode is incorrect, "Access Denied" is displayed, the RGB LED glows red, and the buzzer remains silent.
4. **Garage Door Control**: After passcode verification, the ultrasonic sensor monitors the garage door's surroundings. If an object is detected within the specified threshold distance, the garage door closes. If the area is clear, the door remains open.
5. **Reset**: After each passcode entry, the system resets to the initial state, prompting the user to enter a new passcode.

### Files
- **Garage_Opener_With_Passcode_verification.ino**: Arduino sketch containing the complete code for the garage opener with passcode verification.
- **README.md**: This README file providing an overview of the project.

### Installation and Setup
1. Connect all components according to the provided circuit diagram.
2. Upload the `Garage_Opener_With_Passcode_verification.ino` sketch to the Arduino board.
3. Open the serial monitor to view system messages and prompts.
4. Follow the on-screen instructions to enter the passcode and operate the garage door.


### Dependencies
- **NewPing Library**: Used for interfacing with the ultrasonic distance sensor.
- **AccelStepper Library**: Required for controlling the stepper motor.
- **LiquidCrystal_I2C Library**: Necessary for controlling the LCD display via the I2C interface.
- **Keypad Library**: Used to interface with the 4x4 keypad.

### Note
Ensure that the keypad wiring and library setup match your specific configuration. Adjust pin assignments and library inclusions accordingly if needed.
