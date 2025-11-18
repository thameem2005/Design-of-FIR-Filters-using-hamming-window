# Design-of-FIR-Filters-using-hamming-window
# DESIGN OF LOW PASS FIR DIGITAL FILTER 
# AIM: 
  To generate design of high pass FIR digital filter using SCILAB 
# APPARATUS REQUIRED: 
  PC Installed with SCILAB 
# PROGRAM 
```
clc ; 
close ; 
M=input('Enter the Odd Filter Length ='); 
Wc=input('Enter the Digital Cut off frequency ='); 
alpha= (M -1)/2  
for n = 1:M  
if (n ==alpha+1) 
hd(n) = Wc/ %pi ; 
else 
hd(n) = sin(Wc *((n -1)-alpha)) /(((n -1)-alpha)*%pi); 
end 
end 
for n = 1:M 
W(n) = 0.54-(0.46*cos((2*%pi*(n-1))/(M-1))); 
end 
h = hd.*W; 
disp(h,'Filter Coefficients are') 
[hzm,fr]= frmag (h,256) ; 
subplot(2 ,1 ,1) 
plot(2*fr, hzm) 
xlabel( ' Normalized Digital Frequency w'); 
ylabel( 'Magnitude '); 
title( ' Frequency Response of FIR LPF using Hamming Window ') 
27 
hzm_dB = 20* log10 (hzm); 
subplot (2 ,1 ,2); 
plot(2*fr , hzm_dB); 
xlabel( ' Normalized Digital Frequency W' ); 
ylabel( 'Magnitude in dB'); 
title('Frequency Response of FIR LPF using Hamming Window'); 
what is the input for this
```
# OUTPUT
<img width="1920" height="1140" alt="508713365-2630d6f7-1dab-434b-bd03-941c951f1fd1" src="https://github.com/user-attachments/assets/e5769096-546f-425f-9bd3-fa235e66c136" />
# RESULT

Thus the design of low pass FIR digital filter was generated using SCILAB.


