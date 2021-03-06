# DigitalCommunication
# Matlab Simulink project about simulattion of the performance of different modulation schemes, BPSK, QPSK, FSK, QAM(16-64) in an AWGN environment.

- General Simulation Steps:
  - setup block diagram with AWGN: Eb/No= 10 db and RandomIntegerGeneration: samplesPerFrame=100 and sourceOfInitialSeed=parameter
  - run simulation for 1000000
  - change AWGN Eb/No to EbNo variable to draw ber vs Eb/No with bertool
  - in ToWorkspace block (simout) set variable name = ber and save format = array and save 2-D signals = 2-D array.
  - open bertool draw therotical set Eb/No range = -10:10 then press plot 
  - then in monte carlo set Eb/No range = -10:1:10 with step 1 
  - finaly set no. of bite to 1e4 then click run.

# Binary Phase Shift Keying (BPSK)
This is called as 2-phase PSK or Phase Reversal Keying. In this technique, the sine wave carrier takes two phase reversals such as 0° and 180°.
BPSK is basically a Double Side Band Suppressed Carrier (DSBSC) modulation scheme, for message being the digital information.

- For BPSK Simulation
  - RandomIntegerGeneration:set size = 2
## Scatter Plot and Performance Diagram 
![bpsk](https://github.com/ahmed1salama/DigitalCommunication/blob/master/bpsk/BPSK%20before%20and%20after%20Noise.PNG)
![bpsk](https://github.com/ahmed1salama/DigitalCommunication/blob/master/bpsk/BPSK%20performance.png)
 
 # Quadrature Phase Shift Keying (QPSK)
This is the phase shift keying technique, in which the sine wave carrier takes four phase reversals such as 0°, 90°, 180°, and 270°.
If this kind of techniques are further extended, PSK can be done by eight or sixteen values also, depending upon the requirement.

- For QPSK Simulation
  - RandomIntegerGeneration:set size = 4

## Scatter Plot and Performance Diagram 
![qpsk](https://github.com/ahmed1salama/DigitalCommunication/blob/master/qpsk/QPSK%20before%20and%20after%20Noise.PNG)
![qpsk](https://github.com/ahmed1salama/DigitalCommunication/blob/master/qpsk/QPSK%20performance.png)

# Frequency Shift Keying (FSK) 
This is the digital modulation technique in which the frequency of the carrier signal varies according to the digital signal changes. FSK is a scheme of frequency modulation.

The output of a FSK modulated wave is high in frequency for a binary High input and is low in frequency for a binary Low input. The binary 1s and 0s are called Mark and Space frequencies. 

- For FSK Simulation
  - RandomIntegerGeneration:set size = 2
  
## Scatter Plot and Performance Diagram 
![fsk](https://github.com/ahmed1salama/DigitalCommunication/blob/master/fsk/Fsk%20before%20and%20after%20Noise.PNG)
![fsk](https://github.com/ahmed1salama/DigitalCommunication/blob/master/fsk/FSK%20performance.png)
  
 
# Quadrature Amplitude Modulation (QAM) -16
This is also antoher modulation scheme but  carry information in amplitude and in phase (only two phases). It uses two carriers sin and cos and recived signal with differnt amplitudes. 
bits per symbol = 4.

- For QAM-16 Simulation
  - RandomIntegerGeneration:set size = 16
  - In modualtor and demodualtor: M-ary number =16

## Scatter Plot and Performance Diagram 
![qam16](https://github.com/ahmed1salama/DigitalCommunication/blob/master/qam16/QAM-16%20before%20and%20after%20Noise.PNG)
![qam16](https://github.com/ahmed1salama/DigitalCommunication/blob/master/qam16/QAM-16%20performance.png)


# Quadrature Amplitude Modulation (QAM) -64
This is the same as QAM-16 but with bits per symbol = 6.

- For QAM-64 Simulation
  - RandomIntegerGeneration:set size = 64
  - In modualtor and demodualtor: M-ary number = 64
  
## Scatter Plot and Performance Diagram 
![qam64](https://github.com/ahmed1salama/DigitalCommunication/blob/master/qam64/QAM-64%20before%20and%20after%20Noise.PNG)
![qam64](https://github.com/ahmed1salama/DigitalCommunication/blob/master/qam64/QAM-64%20performance.png)
 
# Note : for rasied cosin ouput i have put the outputs and the diagram in a separate folder called raised cosin but i found that the ber became worse rather than becoming better after raised cosin so i didn't put it in the readme.md
