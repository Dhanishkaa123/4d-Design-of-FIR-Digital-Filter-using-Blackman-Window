# FIR-FILTER-DESIGN
# EXP 4 d: Design-of-FIR-Digital-Filter-using-Blackman-Window

# AIM 1:  To perform Design-of-LOWPASS FIR-Digital-Filter-using-Blackman-Window using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
    // FIR HPF using Hamming Window

    clc;
    clear;
    close;

    // Input values
    M = input("Enter the Odd Filter Length = ");
    Wc = input("Enter the Digital Cut off frequency = ");

    alpha = (M-1)/2;     // Center value

       // Ideal High Pass Filter impulse response
     for n = 1:M
    if (n == alpha + 1) then
        hd(n) = 1 - Wc/%pi;
    else
        hd(n) = -sin(Wc*((n-1)-alpha))/(((n-1)-alpha)*%pi);
    end
    end

     // Hamming Window
     for n = 1:M
    W(n) = 0.54 - 0.46*cos((2*%pi*(n-1))/(M-1));
     end

     // Windowed filter coefficients
    h = hd .* W;

    disp("Filter Coefficients are");
    disp(h);

     // Frequency response
    [hz, fr] = frmag(h,256);

    // Magnitude plot
    subplot(2,1,1)
    plot(2*fr, hz)
    xlabel("Normalized Digital Frequency W")
    ylabel("Magnitude")
    title("Frequency Response of FIR HPF using Hamming Window")

    // Magnitude in dB
    hz_dB = 20*log10(hz);

    subplot(2,1,2)
    plot(2*fr, hz_dB)
     xlabel("Normalized Digital Frequency W")
    ylabel("Magnitude in dB")
    title("Frequency Response of FIR HPF using Hamming Window")


# OUTPUT: 

<img width="975" height="577" alt="image" src="https://github.com/user-attachments/assets/2e73e786-a80e-45ae-bb34-dfe60a0342d5" />

# RESULT: 

Thus design of low pass FIR digital filter using-Blackman-Window waveforms were plotted and output was verified.

# AIM 2: To perform DESIGN OF HIGH PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
 // FIR HPF using Hamming Window

    clc;
    clear;
    close;

    // Input values
    M = input("Enter the Odd Filter Length = ");
    Wc = input("Enter the Digital Cut off frequency = ");

    alpha = (M-1)/2;     // Center value

       // Ideal High Pass Filter impulse response
     for n = 1:M
    if (n == alpha + 1) then
        hd(n) = 1 - Wc/%pi;
    else
        hd(n) = -sin(Wc*((n-1)-alpha))/(((n-1)-alpha)*%pi);
    end
    end

     // Hamming Window
     for n = 1:M
    W(n) = 0.54 - 0.46*cos((2*%pi*(n-1))/(M-1));
     end

     // Windowed filter coefficients
    h = hd .* W;

    disp("Filter Coefficients are");
    disp(h);

     // Frequency response
    [hz, fr] = frmag(h,256);

    // Magnitude plot
    subplot(2,1,1)
    plot(2*fr, hz)
    xlabel("Normalized Digital Frequency W")
    ylabel("Magnitude")
    title("Frequency Response of FIR HPF using Hamming Window")

    // Magnitude in dB
    hz_dB = 20*log10(hz);

    subplot(2,1,2)
    plot(2*fr, hz_dB)
     xlabel("Normalized Digital Frequency W")
    ylabel("Magnitude in dB")
    title("Frequency Response of FIR HPF using Hamming Window")

# OUTPUT: 
<img width="975" height="577" alt="image" src="https://github.com/user-attachments/assets/c5bf0fa0-3649-4e15-9396-3285302dfad1" />


# RESULT: 
Thus design of HIGH pass FIR digital filter using-Blackman-Window waveforms were plotted and output was verified.

# AIM 3: To perform DESIGN OF BAND PASS FIR DIGITAL FILTERS using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
 // FIR HPF using Hamming Window

    clc;
    clear;
    close;

    // Input values
    M = input("Enter the Odd Filter Length = ");
    Wc = input("Enter the Digital Cut off frequency = ");

    alpha = (M-1)/2;     // Center value

       // Ideal High Pass Filter impulse response
     for n = 1:M
    if (n == alpha + 1) then
        hd(n) = 1 - Wc/%pi;
    else
        hd(n) = -sin(Wc*((n-1)-alpha))/(((n-1)-alpha)*%pi);
    end
    end

     // Hamming Window
     for n = 1:M
    W(n) = 0.54 - 0.46*cos((2*%pi*(n-1))/(M-1));
     end

     // Windowed filter coefficients
    h = hd .* W;

    disp("Filter Coefficients are");
    disp(h);

     // Frequency response
    [hz, fr] = frmag(h,256);

    // Magnitude plot
    subplot(2,1,1)
    plot(2*fr, hz)
    xlabel("Normalized Digital Frequency W")
    ylabel("Magnitude")
    title("Frequency Response of FIR HPF using Hamming Window")

    // Magnitude in dB
    hz_dB = 20*log10(hz);

    subplot(2,1,2)
    plot(2*fr, hz_dB)
     xlabel("Normalized Digital Frequency W")
    ylabel("Magnitude in dB")
    title("Frequency Response of FIR HPF using Hamming Window")

# OUTPUT: 
<img width="975" height="577" alt="image" src="https://github.com/user-attachments/assets/e88f4a10-08d9-4ff8-9ed1-00404f497acf" />


# RESULT: 
Thus design of BAND pass FIR digital filter using-Blackman-Window waveforms were plotted and output was verified.

# AIM 4: To perform DESIGN OF BAND STOP FIR DIGITAL FILTER using SCILAB.

# APPARATUS REQUIRED: 
PC installed with SCILAB. 

# PROGRAM: 
 // FIR HPF using Hamming Window

    clc;
    clear;
    close;

    // Input values
    M = input("Enter the Odd Filter Length = ");
    Wc = input("Enter the Digital Cut off frequency = ");

    alpha = (M-1)/2;     // Center value

       // Ideal High Pass Filter impulse response
     for n = 1:M
    if (n == alpha + 1) then
        hd(n) = 1 - Wc/%pi;
    else
        hd(n) = -sin(Wc*((n-1)-alpha))/(((n-1)-alpha)*%pi);
    end
    end

     // Hamming Window
     for n = 1:M
    W(n) = 0.54 - 0.46*cos((2*%pi*(n-1))/(M-1));
     end

     // Windowed filter coefficients
    h = hd .* W;

    disp("Filter Coefficients are");
    disp(h);

     // Frequency response
    [hz, fr] = frmag(h,256);

    // Magnitude plot
    subplot(2,1,1)
    plot(2*fr, hz)
    xlabel("Normalized Digital Frequency W")
    ylabel("Magnitude")
    title("Frequency Response of FIR HPF using Hamming Window")

    // Magnitude in dB
    hz_dB = 20*log10(hz);

    subplot(2,1,2)
    plot(2*fr, hz_dB)
     xlabel("Normalized Digital Frequency W")
    ylabel("Magnitude in dB")
    title("Frequency Response of FIR HPF using Hamming Window")

# OUTPUT: 
<img width="975" height="577" alt="image" src="https://github.com/user-attachments/assets/d0fc5454-37e0-481e-b71c-1c0ec5f16665" />


# RESULT: 
Thus design of BAND STOP FIR digital filter using-Blackman-Window waveforms were plotted and output was verified.
