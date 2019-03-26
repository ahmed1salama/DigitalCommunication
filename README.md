# DigitalCommunication
# Matlab Simulink project about simulattion of the performance of different modulation schemes, BPSK, QPSK, FSK, QAM(16-64) in an AWGN environment.

- General Simulation Steps:
  - setup block diagram with AWGN: Eb/No= 10 db and RandomIntegerGeneration: samples per frame = 100
  - run simulation for 1000000
  - change AWGN Eb/No to EbNo variable to draw ber vs Eb/No with bertool
  - open bertool draw therotical set Eb/No range -10:10 then press plot 
  - then in monte carlo set Eb/No range to be -10:1:10 with step 1 
  - finaly set no. of bite to 1e4 then click run.
