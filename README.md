# Advanced Light Sensing System with Rotating Shaft Meter

This Arduino project features an advanced light sensing system equipped with a rotating shaft meter to visually display the intensity of light. The system comprises two light detectors (photoresistors), a self-illuminating LED, and a danger alert system with a buzzer for immediate alerts.


(https://github.com/phpandya28/advance-light-sesing-system/assets/138100019/2c7f693d-8753-42fa-80a0-fc0615c6c517)

## Components Used
- Arduino board
- Servo motor for the rotating shaft meter
- Two photoresistors (connected to A1 and A2)
- Self-illuminating LED (connected to digital pin 8)
- Danger alert buzzer (connected to digital pin 4)
- Danger alert LED (connected to digital pin 7)

## Wiring
- Connect the servo motor to pin 2.
- Connect two photoresistors to analog pins A1 and A2.
- Connect the self-illuminating LED to digital pin 8.
- Connect the danger alert buzzer to digital pin 4.
- Connect the danger alert LED to digital pin 7.

## Code Explanation
1. **Servo Initialization:**
   - The Servo library is used to control the servo motor connected to pin 2.

2. **Photoresistor and Voltage Reading:**
   - Two photoresistors are read from analog pins A1 and A2.
   - The average voltage reading is calculated as `voltageread = (voltageread1 + voltageread2)/2`.

3. **Rotating Shaft Meter:**
   - The servo motor position is determined based on the average voltage reading, creating a rotating shaft meter to visually represent light intensity.

4. **Alert System:**
   - If the light intensity drops below a threshold (voltageread < 15), both the danger alert LED and buzzer are activated for a specified duration.

5. **LED Brightness Control:**
   - The self-illuminating LED's brightness is controlled using PWM based on the average voltage reading.

## Setup
1. Connect the components following the specified wiring.
2. Upload the provided code to your Arduino board.
3. Observe the rotating shaft meter and alert system response to changes in light intensity.

## Additional Notes
- Adjust the threshold value (15 in this code) based on your specific requirements.
- Experiment with different threshold values and observe how the system responds to varying light conditions.

Feel free to modify and extend the code to suit your preferences and project requirements. This project provides a versatile foundation for creating advanced light sensing and alert systems.
