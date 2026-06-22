# Radar-range
**Aim:**

To calculate the maximum range of a radar system using the Radar Range Equation and verify the results through Python programming.
**Theory:**

The Radar Range Equation is a fundamental formula used in radar system design to determine the maximum range at which a radar can detect a target. It is given by:

<img width="457" height="424" alt="image" src="https://github.com/user-attachments/assets/3e23c7ac-0007-43e6-b546-3ac395847206" />

**Procedure:**


1.Set Up the Python Environment: Ensure that Python is installed on your system. You can use Anaconda for managing Python packages and environments, or any other Python IDE of your choice. 2.Import Necessary Libraries: Import the math library in Python. 3.Define the Radar Range Equation Function: Create a function to calculate the maximum range using the Radar Range Equation. 4.Input Parameters for the Radar System: Define the input parameters such as transmitted power, transmitter gain, receiver gain, radar frequency, radar cross section, and minimum detectable power. 5.Calculate the Maximum Range: Use the function to calculate the maximum range of the radar. 6.Execute the Program: Run the Python script to calculate and display the maximum range of the radar.

**Program:**
```
Gt = 100;
Gr = 100;
lambda = 0.03;
sigma = 1;
R = 100:100:10000;
Pt = 1000;
Pr = (Pt*Gt*Gr*(lambda^2)*sigma) ./ (((4*%pi)^3)*(R.^4));
Pr_dB = 10*log10(Pr);
Pr_min = 1e-12;
Pt_req = (Pr_min*((4*%pi)^3).*(R.^4)) ./ (Gt*Gr*(lambda^2)*sigma);
Pt_dB = 10*log10(Pt_req);
figure(1);
plot(R,Pr_dB);
xlabel("Range R (m)");
ylabel("Received Power Pr (dB)");
title("Pr (dB) vs Range");
xgrid();
figure(2);
plot(R,Pt_dB);
xlabel("Range R (m)");
ylabel("Transmitted Power Pt (dB)");
title("Pt (dB) vs Range");
xgrid();
```

**Output Waveform:**
<img width="1918" height="1198" alt="image" src="https://github.com/user-attachments/assets/28239358-e35e-497c-967f-d7510e2b451c" />



**Tabulation:**
<img width="1600" height="1105" alt="image" src="https://github.com/user-attachments/assets/cd963b46-993f-4d13-afa1-77067a889345" />


**Result:**
Thus, the maximum range of a radar system calculated using the Radar Range Equation is successfully verified using Scilab programming.
