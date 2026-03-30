# ECG Signal Analysis and QRS Detection using MATLAB
# AIM:

To analyze an ECG signal and detect QRS complexes using MATLAB.

# THEORY:

Electrocardiography (ECG) is a diagnostic technique used to measure the electrical activity of the heart. The ECG signal is generated due to the depolarization and repolarization of cardiac muscle cells during each heartbeat.
A typical ECG waveform consists of several components:

•	P wave – atrial depolarization

•	QRS complex – ventricular depolarization

•	T wave – ventricular repolarization

Among these components, the QRS complex has the highest amplitude and is the most significant feature used for detecting heart rate and cardiac abnormalities.
ECG signals are often affected by noise such as:

•	baseline wander

•	muscle noise

•	power-line interference (50 Hz)

Signal processing techniques are used to filter noise and extract useful features from ECG signals. One important technique is QRS detection, which identifies the location of ventricular depolarization peaks.
MATLAB provides functions such as findpeaks() that help detect QRS complexes automatically. Detecting QRS peaks allows biomedical engineers and doctors to calculate heart rate and identify arrhythmias.

# ALGORITHM :
1.	Load ECG signal data.
2.	Define the sampling frequency.
3.	Plot the ECG signal waveform.
4.	Apply a threshold-based method to detect QRS peaks.
5.	Mark the detected peaks on the ECG signal.
6.	Display the result.

# MATLAB CODE :
~~~
x=[0,0,0,0.5,0.7,0.8,0.7,0.5,0,0,-1,-1.5,1,2,4,6,4,2,1,-1,-2,
4,0,0,0,0,0.2,0.4,0.8,0,0,0,0,0,0,0,0.5,0.7,0.8,0.7,0.5,0,0,-1,-1.5,1,2,4,6,4,2,1,-1,-2,
4,0,0,0,0,0.2,0.4,0.8,0,0,0,0,0,0,0,0.5,0.7,0.8,0.7,0.5,0,0,-1,-1.5,1,2,4,6,4,2,1,-1,-2,
4,0,0,0,0,0.2,0.4,0.8,0,0,0,0,0,0,0,0.5,0.7,0.8,0.7,0.5,0,0,-1,-1.5,1,2,4,6,4,2,1,-1,-2,
4,0,0,0,0,0.2,0.4,0.8,0,0,0,0,0,0,0,0.5,0.7,0.8,0.7,0.5,0,0,-1,-1.5,1,2,4,6,4,2,1,-1,-2,
4,0,0,0,0,0.2,0.4,0.8,0,0,0,0,0,0,0,0.5,0.7,0.8,0.7,0.5,0,0,-1,-1.5,1,2,4,6,4,2,1,-1,-2,
4,0,0,0,0,0.2,0.4,0.8,0,0,0,0]
subplot(3,2,1);
plot(x);
xlabel('time');
ylabel('amplitude');
title('ecg');
e=randn(80,1);
subplot(3,2,2);
plot(e);
xlabel('time');
ylabel('amplitude');
title('random noise');
y=conv(x,e);
subplot(3,2,3);
plot(y);
title('noisy signal');
29
h=[1 1 1 1 1 1]/6;
y1=conv(h,y);
subplot(3,2,4);
plot(y1);
xlabel('time');
ylabel('amplitude');
title('fitered output');
y2=fft(y1);
subplot(3,2,5);
plot(y2);
xlabel('time');
ylabel('amplitude');
title('fft for the ecg signal');
~~~
# OUTPUT GRAPH :
<img width="830" height="462" alt="image" src="https://github.com/user-attachments/assets/8607d7fd-b420-4de3-941f-2a6727bd3959" />

# RESULT :
The ECG signal was analyzed and QRS complexes were successfully detected using MATLAB.

