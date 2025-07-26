# VTOL_Lift_Control Using SIMULINK
This project models and simulates the vertical lift control of a VTOL (Vertical Take-Off and Landing) aircraft using a PID controller in Simulink. The system aims to demonstrate how a VTOL responds to altitude commands by managing thrust while compensating for gravity.

🚀 Overview

Simulation Type: Altitude control (1D vertical motion)

Controller Used: PID

Platform: MATLAB Simulink

Focus: VTOL lift dynamics, PID feedback loop, gravity compensation

📊 Output Summary

The simulation shows how the VTOL responds to a lift command. The aircraft lifts off, reaches a peak altitude (~18 m), and exhibits smooth oscillations before gradually stabilizing. This indicates an underdamped but stable system controlled by the PID loop.

🧱 Model Components

Battery Input (48V equivalent) – Supplies reference input

PID Controller – Adjusts thrust based on altitude error

Gain Blocks – Model motor scaling and force-to-acceleration conversion

Gravity Compensation – Adds 49.05 N to offset weight of a 5 kg VTOL

Integrators – Compute velocity and altitude over time

Scope – Visualizes altitude response

🔁 Control Loop Description

Desired altitude is set via constant input.

Error is calculated by subtracting feedback from the desired value.

PID processes this error and outputs control effort.

Thrust is scaled and gravity is added to get net force.

The force is converted to acceleration (F = ma), integrated to get velocity and then position.

The altitude is fed back to close the loop.

📂 Files

vtol_lift_control.slx – Simulink model file

output_graph.png – Altitude vs. Time response graph

README.md – Project documentation

🛠️ Future Improvements

Tune PID parameters to reduce oscillations

Extend to 3D motion control (pitch, roll, yaw)

Integrate with full eVTOL simulation environment

📧 Contact

For suggestions or collaboration:
Author: Madan SEmail: [smadan0330@gmail.com]
