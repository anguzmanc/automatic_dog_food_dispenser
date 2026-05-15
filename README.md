<h1 align="center">🐶 Automatic Dog Food Dispenser</h1>

<p align="center">
An FPGA-based automatic dog food dispenser developed using Verilog HDL and digital electronics.
</p>

<hr>

<h2>📌 Project Overview</h2>

<p>
This project focuses on simplifying the task of feeding dogs through the design and implementation of an automated food dispenser prototype.
</p>

<p>The system is capable of:</p>

<ul>
  <li>Dispensing food automatically at scheduled intervals</li>
  <li>Monitoring the remaining food level</li>
  <li>Indicating food availability through LEDs</li>
  <li>Reducing the effort required from pet owners</li>
</ul>

<hr>

<h2>📊 Context and Motivation</h2>

<ul>
  <li>Around <b>3 million dogs and cats</b> are abandoned in Colombia.</li>
  <li>Bogotá alone has approximately <b>66,000 stray dogs</b>.</li>
</ul>

<p>
These numbers motivated the exploration of automated feeding mechanisms that could eventually be adapted for shelters or community feeding stations.
</p>

<hr>

<h2>🎯 Objectives</h2>

<h3>Main Objective</h3>

<p>
Design and implement a dog food dispenser that addresses the identified issues by utilizing digital electronics and the knowledge gained in class.
</p>

<h3>Secondary Objective</h3>

<p>
Explore the possibility of adapting the system to help animals in abandonment conditions.
</p>

<h3>Specific Objectives</h3>

<ul>
  <li>Meet the minimum input/output requirements of the project</li>
  <li>Develop a functional prototype</li>
  <li>Achieve energy-efficient operation</li>
  <li>Implement reliable peripheral control systems</li>
</ul>

<hr>

<h2>⚙️ System Inputs and Outputs</h2>

<h3>Inputs</h3>

<table>
  <tr>
    <th>Component</th>
    <th>Function</th>
  </tr>
  <tr>
    <td>Ultrasonic Sensor</td>
    <td>Detects food level inside the container</td>
  </tr>
  <tr>
    <td>Timer / Clock</td>
    <td>Controls scheduled food dispensing</td>
  </tr>
</table>

<br>

<h3>Outputs</h3>

<table>
  <tr>
    <th>Component</th>
    <th>Function</th>
  </tr>
  <tr>
    <td>Servo Motor</td>
    <td>Opens and closes the food gate</td>
  </tr>
  <tr>
    <td>LED Indicators</td>
    <td>Display food level status</td>
  </tr>
</table>

<hr>

<h2>🛠️ Technologies Used</h2>

<ul>
  <li>Verilog HDL</li>
  <li>FPGA myStorm BlackIce Mx</li>
  <li>Ultrasonic Sensor</li>
  <li>Servo Motor</li>
  <li>Digital Electronics</li>
  <li>RTL Design</li>
</ul>

<hr>

<h2>🧩 Project Implementation</h2>

<p>
The project was developed by independently implementing and testing both peripherals:
</p>

<ul>
  <li>Ultrasonic sensor module</li>
  <li>Servo motor gate control</li>
</ul>

<p>
Each module achieved proper standalone functionality and was adjusted according to the physical dimensions of the dispenser prototype.
</p>

<p>
The repository includes separate directories for each subsystem implementation.
</p>

<hr>

<h2>⚠️ Main Challenge</h2>

<p>
The primary issue encountered during development was integrating both peripherals into a single FPGA design operating simultaneously.
</p>

<p>
Although:
</p>

<ul>
  <li>Individual Verilog modules compiled correctly</li>
  <li>RTL schematics showed valid connections</li>
  <li>Syntax and FPGA interpretation errors were corrected</li>
</ul>

<p>
The servo motor began malfunctioning after integration:
</p>

<ul>
  <li>Producing continuous buzzing sounds</li>
  <li>Experiencing overload behavior</li>
  <li>Damaging two servo motors during testing</li>
</ul>

<p>
Due to time and hardware limitations, the final prototype demonstration was performed with each peripheral operating independently.
</p>

<hr>

<h2>🎥 Demonstration Videos</h2>

<h3>Final Dispenser Prototype</h3>

<p>Add video or GIF here</p>

<h3>Ultrasonic Sensor Test</h3>

<p>Add video or GIF here</p>

<h3>Servo Motor Failure Demonstration</h3>

<p>Add video or GIF here</p>

<hr>

<h2>📚 Lessons Learned</h2>

<p>
This project strengthened practical knowledge in:
</p>

<ul>
  <li>Digital system design</li>
  <li>FPGA development</li>
  <li>Verilog HDL programming</li>
  <li>Peripheral interfacing</li>
  <li>Hardware debugging</li>
</ul>

<p>
Although full integration was not successfully completed, the project provided valuable experience for future embedded systems and FPGA-based developments.
</p>

<hr>

<h2>📖 References</h2>

[1] Chacón, P. “Hay 3 millones de perros y gatos abandonados en Colombia: este es el plan que propone la senadora Andrea Padilla para cambiar esta realidad”, infobate. Accessed October 6, 2023. Available [online] : https://www.infobae.com/colombia/2023/01/31/hay-3-millones-de-perros-y-gatos-abandonados-en-colombia-este-es-el-plan-que-propone-la-senadora-andrea-padilla-para-cambiar-esta-realidad/ 

[2] Redacción Semana. “Día del Perro Callejero: más de 66.000 caninos deambulan por las calles de Bogotá”, Semana. Accessed October 6, 2023. Available [online] : https://www.semana.com/nacion/articulo/dia-del-perro-callejero-mas-de-66000-caninos-deambulan-por-las-calles-de-bogota/202306/  

<hr>
