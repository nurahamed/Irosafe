# Irosafe
Automatic power cut-off for the iron machine, triggered by the user’s absent mind, ensures safety

### Analog Input LED Control
#### Overview

This Arduino project utilizes an analog sensor (potentiometer, light sensor, etc.) to control an LED. The LED stays on as long as there is analog input detected. If there is no input for 3 seconds, the LED turns off.

#### Components

1. **Analog Input Pin (A0):**
   - Connect an analog sensor to this pin. The code reads the analog value from this pin to detect input.

2. **LED Pin (6):**
   - Connect an LED to this digital output pin. The LED state is controlled based on the analog input.

3. **Interval (3000 milliseconds):**
   - Set the interval to 3000 milliseconds (3 seconds). If no analog input is detected within this time, the LED turns off.

#### Variables

- **`analogInputPin`:**
  - Specifies the analog pin where the sensor is connected.

- **`ledPin`:**
  - Specifies the digital pin where the LED is connected.

- **`interval`:**
  - Sets the time interval (3 seconds) for which the LED stays on without analog input.

- **`lastInputTime`:**
  - Stores the time of the last analog input. Updated whenever input is detected.

- **`ledState`:**
  - Represents the current state of the LED (ON/OFF).

#### Setup Function

- **`setup()`:**
  - Initializes the LED pin as an output and sets the initial LED state.
  - Serial communication is initialized for debugging.

#### Loop Function

- **`loop()`:**
  - Reads the analog input value from the sensor.
  - Prints the analog value to the Serial Monitor.
  - If analog input is detected, updates the `lastInputTime` and keeps the LED on.
  - Checks if 3 seconds have passed since the last input. If so, turns off the LED.

#### Operation

1. **Analog Input Detection:**
   - The code continuously reads the analog input value.
   - If the analog value is greater than 0, it indicates input, and the LED stays on.

2. **LED Off After 3 Seconds:**
   - If no input is detected for 3 seconds, the LED turns off.

3. **Serial Communication:**
   - Analog values and status messages are printed to the Serial Monitor for debugging.

#### How to Use

1. Connect an analog sensor to the A0 pin.
2. Connect an LED to pin 6.
3. Upload the code to your Arduino board.
4. Open the Serial Monitor to view analog values and status messages.
5. Observe the LED behavior based on analog input.

#### How to Contribute

1. Fork the repository.
2. Create a branch: `git checkout -b feature/new-feature`.
3. Make changes and commit: `git commit -m 'Add new feature'`.
4. Push to the branch: `git push origin feature/new-feature`.
5. Create a pull request.

#### License

This project is licensed under the [MIT License](LICENSE).

Feel free to customize this template according to your specific project details and requirements.
