# Project---WIS-Python-course

This project is a program to calculate the adiabatic fraction (AF) in a cloud.

### short introduction
Clouds consist of adiabatic (undiluted) and non-adiabatic parts. The adiabatic fraction (AF) is a measure of adiabaticity and, hence, of mixing.
The AF is defined as $LWC/LWC_{ad}$, where $LWC_{ad}$ is the liquid water content that a parcel would gain while being lifted adiabatically from the cloud base. [Eytan at el. (2021)](https://acp.copernicus.org/articles/21/16203/2021/acp-21-16203-2021.html) tested different methods to calculate AF values by comparing them to an Eulerain passive tracer. The method found to be the most accurate follows the analytical derivation of [Korolev and Mazin (2003)](https://journals.ametsoc.org/view/journals/atsc/60/24/1520-0469_2003_060_2957_sowvic_2.0.co_2.xml?tab_body=abstract-display) of the supersaturation in an adiabatic ascending parcel while changing the time domain to vertical coordinates (and changing $q_w = \frac{LWC}{\rho_d}$).

 $\frac{dlog(S+1)}{dz}=A_1-A_2\frac{dLWC}{dz}$


$A_1=\frac{g}{T}(\frac{L_w}{c_pR_vT}-\frac{1}{R_a})$

$A_2=\frac{1}{\rho_v}+\frac{L_w^2}{c_pR_vT^2\rho_d}$ 

