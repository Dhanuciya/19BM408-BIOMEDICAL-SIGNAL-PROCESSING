# COMPUTATION OF DISCRETE FOURIER TRANSFORM (DFT) OF A DISCRETE-TIME SIGNAL
#  Aim :
To compute and plot the Discrete Fourier Transform (DFT) of a given discrete-time signal using MATLAB.
# Apparatus / Software Required:
•	Computer / Laptop

•	MATLAB software
# Theory :
A discrete-time signal may contain multiple frequency components.
The Discrete Fourier Transform (DFT) converts a signal from the time domain into the frequency domain and shows the strength of each frequency present in the signal.
MATLAB computes DFT efficiently using the Fast Fourier Transform (FFT) algorithm.

Mathematical Expression:
X(k)=∑_(n=0)^(N-1)▒〖x(n)" " 〗 e^(-j2πkn/N)

Where:
	x(n)→ input signal.
  X(k)→ frequency spectrum.
  N→ number of samples.

# Algorithm :
	1) Start the program
	2) Define the discrete-time signal x(n)
	3) Find the length of the signal
	4) Compute the DFT using fft()
	5) Calculate magnitude spectrum using abs()
	6) Plot the DFT using stem()
	7)Stop the program

# MATLAB CODE :
~~~
% Computation of DFT of a Discrete-Time Signal

clc;
clear;
close all;

% Input discrete-time signal
x = [1 1 1 1];

% Length of the signal
N = length(x);

% Compute DFT using FFT
X = fft(x);

% Display DFT values
disp('DFT of the given signal is:');
disp(X);

% Frequency index
k = 0:N-1;

% Plot magnitude spectrum
figure;
stem(k, abs(X), 'filled');
xlabel('Frequency index k');
ylabel('|X(k)|');
title('Magnitude Spectrum of DFT');
grid on;
~~~


# OUTPUT GRAPH :
<img width="919" height="489" alt="image" src="https://github.com/user-attachments/assets/ecbbe474-b46f-4d12-ab12-dcacb566822f" />

# Result :
Thus, the Discrete Fourier Transform of the given discrete-time signal was successfully computed and plotted using MATLAB.



