<h1>Automatic Solar Irrigation System</h1><br>
<div class="introduction">
<p>Automatic solar irrigation systems represent a sustainable and efficient solution for modern agriculture, harnessing the power of the sun to optimize water use for crops. This system integrates solar energy with automated irrigation mechanisms, offering a smart, eco-friendly alternative to traditional irrigation methods that rely on fossil fuels or electrical grids.

The core idea behind automatic solar irrigation is to use solar panels to generate electricity, which powers irrigation pumps and controls the irrigation system. These systems are often equipped with sensors, such as soil moisture or weather sensors, that detect the soil's moisture level, environmental conditions, or rainfall. Based on real-time data, the system automatically adjusts the water supply to the crops, ensuring they receive the right amount of water at the right time, while minimizing water wastage.
<ul>
Key benefits of automatic solar irrigation include:

<li>Sustainability: Solar energy is renewable, reducing reliance on non-renewable power sources.
Water Conservation: Intelligent sensors and automated controls help optimize water usage, preventing over-irrigation and ensuring efficient use of available water.</li>

<li>Cost Efficiency: After the initial setup, the system reduces ongoing costs by eliminating electricity bills and decreasing manual labor.</li>

<li>Remote Monitoring: With modern advancements, many systems allow remote control and monitoring via mobile apps or web platforms, providing farmers with easy access to system status and control, even from a distance.</li>
<li>Environmental Benefits: By reducing water waste and relying on clean energy, solar irrigation contributes to sustainable farming practices and helps mitigate environmental challenges like water scarcity and energy consumption.</li>
</p></div>

<div id="components">
<ol>
<li>Arduino</li>
<li>5v Relay</li>
<li>Submersive motor</li>
<li>Humidity sensor</li>
</ol>
</div>

<div id="construction">
<p>
<ul>

<li>Pin Setup:Pin 3 is used to control the relay, which in turn controls the water supply.
Pin 6 is used to read the status from a soil moisture sensor.</li>
<li>Water Level Detection:The digitalRead(6) function checks the state of the soil sensor.
If the soil is wet (water == HIGH), the relay is turned off (digitalWrite(3, LOW)), stopping the water supply.
If the soil is dry (water == LOW), the relay is turned on (digitalWrite(3, HIGH)), allowing the water supply to continue.</li>
<li>Delay:A delay of 400 milliseconds is added to reduce the possibility of toggling the relay too rapidly.</li>
<li>Possible Improvements:
Debouncing: If the sensor reads noise or fluctuates quickly, consider adding a debounce logic to smooth out the signal.
Analog Sensor: If you're using an analog sensor instead of a digital one, you would use analogRead(6) and adjust your logic based on the analog value to define when the soil is sufficiently dry or wet.
</li>
</p>
</div>

<img src="How to make plant watering system.jpg" height="500px">



