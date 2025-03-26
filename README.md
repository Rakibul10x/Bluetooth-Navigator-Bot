<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bluetooth Navigator Bot</title>
</head>
<body>

<h1 align="center">🤖 Bluetooth Navigator Bot</h1>
<h2 align="center">📲 Smart Wireless Control for Robotic Navigation</h2>

<hr>

<h2>🔍 The Problem</h2>
<p>In many scenarios, such as maze-solving competitions, warehouse navigation, or educational projects, controlling a robot remotely with precision can be challenging. A reliable, Bluetooth-controlled robot offers a flexible and interactive solution for navigation tasks.</p>

<hr>

<h2>💡 The Smart Solution</h2>
<p><b>Bluetooth Navigator Bot</b> is an Arduino-powered robot designed to navigate rooms, corridors, or obstacle paths based on Bluetooth commands. Using a smartphone app, users can instruct the robot to move forward, turn left or right, or stop — ensuring accurate movement control.</p>

<hr>

<h2>🚀 Features</h2>
<ul>
    <li>✅ <b>Wireless Control</b> – Controlled via Bluetooth-enabled smartphone app.</li>
    <li>✅ <b>Precise Navigation</b> – Customizable room-based movement logic.</li>
    <li>✅ <b>Educational Focus</b> – Ideal for STEM learning and robot programming.</li>
    <li>✅ <b>Expandable Design</b> – Supports additional sensors or modules for enhanced features.</li>
    <li>✅ <b>Customizable Commands</b> – Pre-programmed yet flexible for code enhancements.</li>
</ul>

<hr>

<h2>🛠️ How It Works</h2>
<ul>
    <li>🔹 Connect the <b>Bluetooth module (HC-05)</b> to the Arduino.</li>
    <li>🔹 Build the circuit with motor drivers and motors for movement control.</li>
    <li>🔹 Use the companion app to send directional commands (e.g., Forward, Left, Right).</li>
    <li>🔹 Arduino decodes the received commands and controls the robot’s movement accordingly.</li>
</ul>

<hr>

<h2>📜 Project Components</h2>
<ul>
    <li><b>Arduino UNO</b></li>
    <li><b>HC-05 Bluetooth Module</b></li>
    <li><b>Motor Driver Module (L298N)</b></li>
    <li><b>DC Motors with Wheels</b></li>
    <li><b>Power Supply (9V Battery)</b></li>
    <li><b>Chassis for Robot Assembly</b></li>
</ul>

<hr>

<h2>🖥️ Arduino Code</h2>
<pre>
#include &lt;AFMotor.h&gt; 

AF_DCMotor motor1(1); 
AF_DCMotor motor2(2); 
char command; 

void setup() {
    Serial.begin(9600); 
}

void loop() {
    if (Serial.available()) {
        command = Serial.read();
        if (command == 'F') { // Forward
            motor1.setSpeed(150);
            motor2.setSpeed(150);
            motor1.run(FORWARD);
            motor2.run(FORWARD);
        } else if (command == 'B') { // Backward
            motor1.run(BACKWARD);
            motor2.run(BACKWARD);
        } else if (command == 'L') { // Left
            motor1.run(BACKWARD);
            motor2.run(FORWARD);
        } else if (command == 'R') { // Right
            motor1.run(FORWARD);
            motor2.run(BACKWARD);
        } else if (command == 'S') { // Stop
            motor1.run(RELEASE);
            motor2.run(RELEASE);
        }
    }
}
</pre>

<hr>

<h2>🏆 Project Outcomes</h2>
<ul>
    <li>🤖 Built a fully functional <b>Bluetooth-controlled robot</b> capable of precise navigation.</li>
    <li>🎯 Developed an <b>interactive learning platform</b> for programming and robotics.</li>
    <li>🔧 Encourages <b>customization and creative expansion</b> for added functionality.</li>
</ul>

<h2>📽️ Project Demos</h2>

<p>Here are some project snapshots:</p>

<table align="center" border="0" cellpadding="10">
    <tr>
        <td align="center">
            <img src="https://github.com/Rakibul10x/Bluetooth-Navigator-Bot/blob/main/Bluetooth%20Navigator%20Car.jpg" alt="Robot in Motion" width="300">
            <p>📸 Robot navigating with Bluetooth commands</p>
        </td>
        <td align="center">
            <img src="Bot_Circuit.jpg" alt="Robot Circuit Design" width="300">
            <p>📸 Internal circuit and wiring setup</p>
        </td>
    </tr>
</table>

<hr>
<h2>🔗 Get Involved & Build Your Own Bluetooth Navigator Bot!</h2>
<p>🚀 <b>Clone the Repository & Start Building:</b></p>
<pre>
git clone https://github.com/YourUsername/Bluetooth-Navigator-Bot.git
</pre>

</body>
</html>
