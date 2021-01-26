# Powertrain modeling with Simulink

*Author: Kexuan Zhai*

## Model the powertrain of a vehicle
---

<div align=center><img src="https://github.com/ZhaiKexuan/Adaptive-Cruise-Control-and-Autonomous-Lane-Keeping/blob/master/imgaes/Picture1.png"/></div>

Aerodynamic Resistance in X-direction:
<div align=center><img src="https://github.com/ZhaiKexuan/Adaptive-Cruise-Control-and-Autonomous-Lane-Keeping/blob/master/imgaes/Picture1.png"/></div>

Tire Rolling Resistance in X-direction:
<div align=center><img src="https://github.com/ZhaiKexuan/Adaptive-Cruise-Control-and-Autonomous-Lane-Keeping/blob/master/imgaes/Picture1.png"/></div>
Where  is the tire rolling resistance coefficient.

Traction calculation through Torque T:
<div align=center><img src="https://github.com/ZhaiKexuan/Adaptive-Cruise-Control-and-Autonomous-Lane-Keeping/blob/master/imgaes/Picture1.png"/></div>
Where R is the radius of front wheel, 0.95 is the transmission efficiency, 8 is the gear ratio.

Force balance in X-direction:
<div align=center><img src="https://github.com/ZhaiKexuan/Adaptive-Cruise-Control-and-Autonomous-Lane-Keeping/blob/master/imgaes/Picture1.png"/></div>

Combine all the equation above, the acceleration can be expressed as:
<div align=center><img src="https://github.com/ZhaiKexuan/Adaptive-Cruise-Control-and-Autonomous-Lane-Keeping/blob/master/imgaes/Picture1.png"/></div>
---

## Simulate the 0-100 km/h acceleration time and top speed

Simulink Model:
<div align=center><img src="https://github.com/ZhaiKexuan/Adaptive-Cruise-Control-and-Autonomous-Lane-Keeping/blob/master/imgaes/Picture1.png"/></div>

Subsystem: Driving Force
<div align=center><img src="https://github.com/ZhaiKexuan/Adaptive-Cruise-Control-and-Autonomous-Lane-Keeping/blob/master/imgaes/Picture1.png"/></div>

Subsystem: Tire Rolling Resistance
<div align=center><img src="https://github.com/ZhaiKexuan/Adaptive-Cruise-Control-and-Autonomous-Lane-Keeping/blob/master/imgaes/Picture1.png"/></div>

Subsystem: Aerodynamic Resistance
<div align=center><img src="https://github.com/ZhaiKexuan/Adaptive-Cruise-Control-and-Autonomous-Lane-Keeping/blob/master/imgaes/Picture1.png"/></div>

Subsystem: Conversion
<div align=center><img src="https://github.com/ZhaiKexuan/Adaptive-Cruise-Control-and-Autonomous-Lane-Keeping/blob/master/imgaes/Picture1.png"/></div>

---

## Plot of the speed changes

<div align=center><img src="https://github.com/ZhaiKexuan/Adaptive-Cruise-Control-and-Autonomous-Lane-Keeping/blob/master/imgaes/Picture2.jpg"/></div>



## Experimental Results

The experimental result at the start line is shown in the figure below:

| Variable  | Value |
| ------------ | ----------- |
|     The top speed of the vehicle    |     233.35 km/h     |
|     The time required for the vehicle to reach 100 km/h     |     8.39 s    |
|     The time required to reach 99% of the top speed     |     25.99 s     |

- The top speed of the vehicle: 233.35 km/h
- The time required for the vehicle to reach 100 km/h: 8.39 s
- The time required to reach 99% of the top speed: 25.99 s










