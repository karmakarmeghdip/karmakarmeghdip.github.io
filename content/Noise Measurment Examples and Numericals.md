### Noise Measurement and Control Examples with Numerical Solutions

#### Noise Frequency Example
**Example:** A sound wave completes 500 cycles in 2 seconds. What is its frequency?

**Solution:**
$$
\text{Frequency} (f) = \frac{\text{Number of cycles}}{\text{Time (seconds)}} = \frac{500}{2} = 250 \, \text{Hz}
$$

#### Noise Pressure Example
**Example:** A sound wave exerts a pressure of 0.002 Pa. Express this in decibels (dB) relative to the reference sound pressure level of $2 \times 10^{-5}$ Pa.

**Solution:**
$$
\text{Sound Pressure Level (SPL)} = 20 \log_{10} \left(\frac{P}{P_0}\right)
$$
where $P = 0.002 \, \text{Pa}$ and $P_0 = 2 \times 10^{-5} \, \text{Pa}$:
$$
\text{SPL} = 20 \log_{10} \left(\frac{0.002}{2 \times 10^{-5}}\right) = 20 \log_{10} (100) = 20 \times 2 = 40 \, \text{dB}
$$

#### Noise Intensity Example
**Example:** A sound wave has a power of $0.001 \, \text{W}$ distributed over an area of $1 \, \text{m}^2$. What is the noise intensity?

**Solution:**
$$
\text{Intensity} (I) = \frac{\text{Power (P)}}{\text{Area (A)}} = \frac{0.001 \, \text{W}}{1 \, \text{m}^2} = 0.001 \, \text{W/m}^2
$$

#### Noise Threshold Limit Value (TLV) Example
**Example:** If the TLV for occupational noise exposure is 85 dB for an 8-hour workday, what is the allowable exposure time if the noise level is 88 dB?

**Solution:**
Using the rule that a 3 dB increase reduces allowable exposure time by half:
$$
\text{New allowable exposure time} = \frac{8 \, \text{hours}}{2} = 4 \, \text{hours}
$$

#### Equivalent Noise Level (Leq) Example
**Example:** Calculate the Leq for a period with the following noise levels: 85 dB for 2 hours, 80 dB for 4 hours, and 75 dB for 2 hours.

**Solution:**
Using the formula:
$$
L_{eq} = 10 \log_{10} \left(\frac{1}{T} \sum_{i=1}^{n} T_i \times 10^{\frac{L_i}{10}}\right)
$$
where $T = 2+4+2 = 8 \, \text{hours}$:
$$
L_{eq} = 10 \log_{10} \left(\frac{1}{8} \left(2 \times 10^{\frac{85}{10}} + 4 \times 10^{\frac{80}{10}} + 2 \times 10^{\frac{75}{10}}\right)\right)
$$
$$
= 10 \log_{10} \left(\frac{1}{8} \left(2 \times 316227.77 + 4 \times 100000 + 2 \times 31622.78\right)\right)
$$
$$
= 10 \log_{10} \left(\frac{1}{8} \left(632455.54 + 400000 + 63245.56\right)\right)
$$
$$
= 10 \log_{10} \left(\frac{1}{8} \times 1095701.1\right)
$$
$$
= 10 \log_{10} (136962.64) \approx 10 \times 5.137 = 51.37 \, \text{dB}
$$

#### L10 (18hr Index) Example
**Example:** Over an 18-hour period, noise levels were recorded and the level exceeded for 10% of the time was found to be 70 dB. What is the L10 (18hr) index?

**Solution:**
The L10 (18hr) index is directly given as 70 dB since it is the noise level exceeded for 10% of the time.

#### Ld (Daytime Noise Level) Example
**Example:** The average noise levels recorded during the day (7 AM to 10 PM) were as follows: 75 dB from 7 AM to 1 PM and 80 dB from 1 PM to 10 PM. Calculate the Ld.

**Solution:**
Using the formula for the average noise level:
$$
L_d = 10 \log_{10} \left(\frac{1}{T} \sum_{i=1}^{n} T_i \times 10^{\frac{L_i}{10}}\right)
$$
where $T = 15 \, \text{hours}$:
$$
L_d = 10 \log_{10} \left(\frac{1}{15} \left(6 \times 10^{\frac{75}{10}} + 9 \times 10^{\frac{80}{10}}\right)\right)
$$
$$
= 10 \log_{10} \left(\frac{1}{15} \left(6 \times 31622.78 + 9 \times 100000\right)\right)
$$
$$
= 10 \log_{10} \left(\frac{1}{15} \left(189736.68 + 900000\right)\right)
$$
$$
= 10 \log_{10} \left(\frac{1089736.68}{15}\right)
$$
$$
= 10 \log_{10} (72649.11) \approx 10 \times 4.861 = 48.61 \, \text{dB}
$$