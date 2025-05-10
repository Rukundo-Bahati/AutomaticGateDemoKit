🚧 Automated Barrier System with Ultrasonic Sensor
This project implements an automated gate/barrier system using an ultrasonic sensor to detect approaching objects (like vehicles or people). When an object is within a specified distance, the system opens a servo-controlled barrier, lights up a blue LED, and triggers a buzzer. After the object moves away, the barrier closes and a red LED is activated.

🛠️ Hardware Components
Arduino Uno (or compatible)

HC-SR04 Ultrasonic Distance Sensor

SG90 Servo Motor

Red LED (Anode/Cathode configuration)

Blue LED

Buzzer

Jumper wires

Breadboard (optional)

⚙️ Pin Configuration
Component	Arduino Pin
Ultrasonic Trigger	D2
Ultrasonic Echo	D3
Red LED Anode	D4
Red LED Cathode	D8
Blue LED Anode	D5
Blue LED Cathode	D7
Servo Motor	D6
Buzzer	D12

🚦 Functional Description
Idle State: Red LED is ON, blue LED and buzzer are OFF, barrier is closed.

Object Detected within 50 cm:

Barrier opens (servo rotates to 90°).

Red LED turns OFF, blue LED turns ON.

Buzzer gives a short beep.

Object Leaves:

After 5 second of no detection, the barrier closes.

Red LED turns ON, blue LED turns OFF.

🧠 Code Behavior
getDistance(): Uses the ultrasonic sensor to measure the distance.

loop(): Continuously checks distance, handles the servo, LEDs, and buzzer based on object proximity.

📝 Customization
Detection Range: Change thresholdDistance to increase or decrease the detection sensitivity.

Servo Angles: Adjust openAngle and closedAngle to match your barrier’s movement.

Delay Before Closing: Modify closeDelay (in milliseconds) to change the idle timeout.

🔐 Safety Note
Make sure your servo and power supply can handle the mechanical load. Improper voltage or overcurrent can damage components.
