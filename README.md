# Experiment-6-Integrate-sensors-to-monitor-vehicle-components

## AIM
To develop an embedded IoT-based predictive maintenance system for an electric vehicle by integrating sensors that monitor battery health, motor temperature, and brake wear and analyze the data for maintenance prediction.
 
## PROCEDURE
1.	Simulate Sensor Data 
o	Generate battery health, motor temperature, and brake wear data.
2.	Analyze Trends 
o	Detect if any sensor crosses predefined maintenance thresholds.
3.	Predict Maintenance Needs 
o	If any component shows abnormal behavior, flag it for preventive maintenance.
4.	Visualize Data with Graphs 
o	Plot sensor readings and highlight maintenance limits.
5.	Display Alerts 
o	Output maintenance warnings based on real-time sensor data analysis.
 
## THEORY
1. Predictive Maintenance in EVs
•	Battery degradation over time affects range and efficiency.
•	Motor overheating can lead to failures if not detected early.
•	Brake wear monitoring ensures vehicle safety.
2. IoT and Data Analytics Role
•	Real-time monitoring of EV components using embedded sensors.
•	Threshold-based predictions help prevent breakdowns.
•	Graphs help visualize component performance over time.

## PROGRAM

## PROGRAM

```matlab
clear; clc; close all;

t = linspace(0,10,100);

b = 100 - 2*t + 3*sin(0.5*t);
m = 40 + 10*sin(t);
w = 5 + 0.3*t + 2*sin(0.3*t);

bt = 60;
mt = 70;
wt = 15;

flag = (b < bt) | (m > mt) | (w > wt);

subplot(3,1,1);
plot(t,b,'b','LineWidth',2);
yline(bt,'r--','Battery Threshold');
title('Battery Health Over Time');
xlabel('Time (s)');
ylabel('Battery Health (%)');
grid on;

subplot(3,1,2);
plot(t,m,'g','LineWidth',2);
yline(mt,'r--','Temp Threshold');
title('Motor Temperature Over Time');
xlabel('Time (s)');
ylabel('Temperature (°C)');
grid on;

subplot(3,1,3);
plot(t,w,'m','LineWidth',2);
yline(wt,'r--','Brake Wear Limit');
title('Brake Wear Over Time');
xlabel('Time (s)');
ylabel('Wear (%)');
grid on;

fprintf('Predictive Maintenance Alert:\n');

if any(flag)
    disp('Maintenance Needed for Vehicle Components!');
else
    disp('All systems are operating within safe limits.');
end
```

## OUTPUT

The MATLAB simulation displays three graphs:

1. Battery Health Over Time
2. Motor Temperature Over Time
3. Brake Wear Over Time

Each graph also displays the corresponding maintenance threshold.

The Command Window displays:

```text
Predictive Maintenance Alert:
All systems are operating within safe limits.
```

If any monitored parameter crosses its predefined threshold, the program displays:

```text
Predictive Maintenance Alert:
Maintenance Needed for Vehicle Components!
```

## RESULT

The MATLAB simulation successfully predicts maintenance needs in an electric vehicle by monitoring battery health, motor temperature, and brake wear. Threshold-based analysis is used to identify abnormal vehicle-component conditions, while graphical visualization provides a clear representation of component health.
## OUTPUT
<img width="1917" height="1015" alt="image" src="https://github.com/user-attachments/assets/b82b579c-1702-4705-a9b4-e521bda3f6dc" />


 
## RESULT
✅ The MATLAB simulation successfully predicts maintenance needs in an electric vehicle.
✅ The system detects potential failures in battery, motor, and brakes.
✅ Graphical analysis provides a clear view of component health.
 



