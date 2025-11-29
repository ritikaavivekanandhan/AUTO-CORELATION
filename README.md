# AUTO-CORELATION
AUTO-CORRELATION-AND-PSD
Aim

Write a program for Autocorrelation and Power Spectral Density (PSD) of signals in Scilab and verify the Wiener–Khinchin relation.

Equipments Needed

Computer with Intel i3 processor (or higher)

Scilab software

Theory

The Wiener–Khinchin theorem states that:

The Power Spectral Density (PSD) of a wide-sense stationary random process is the Fourier Transform of its autocorrelation function.

This relationship bridges the time-domain correlation and frequency-domain power representations of a signal.

Algorithm

Load or Define the Signal: Input your time-domain signal.

Compute Autocorrelation: Calculate the autocorrelation function of the signal.


Compute Power Spectral Density (PSD):

Estimate the PSD using either:

Fourier Transform of the autocorrelation function, or

Methods like Welch’s periodogram.

Plot Results: Visualize both the autocorrelation function and PSD.

Procedure

Refer to the algorithm and write the code for the experiment.

Open Scilab on your system.

Type your code in a new editor.

Save the file.

Execute the code.

If any errors occur, debug and re-run the program.

Verify the generated waveform using tabulation and model waveform comparison.

Program
~~~
clc
clear all; 
t=0:0.01:2*%pi;
x=sin(2*t) + cos(3*t); 
subplot(3,2,1); 
plot(x); 
au=xcorr(x,x);
subplot (3,2,2); 
plot (au); 
v=fft(au); 
subplot(3,2,3);
plot(abs(v)); 
fw=fft(x); 
subplot(3,2,4); 
plot(fw); 
fw2=(abs(fw)).^2;
subplot(3,2,5); 
plot(fw2);
~~~
Output:

<img width="1920" height="1200" alt="Screenshot (128)" src="https://github.com/user-attachments/assets/d669afdd-4f7e-4658-9e6a-75dc57ba9670" />

![WhatsApp Image 2025-11-29 at 15 50 11](https://github.com/user-attachments/assets/d56399f5-8dbe-4266-9a3a-5c8e88f03133)


Result:

Thus the Autocorrelation and PSD are executed in Scilab and output is verified.

