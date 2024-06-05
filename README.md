# Project---WIS-Python-course

This project is a program to calculate the adiabatic fraction (AF) in a cloud.

### Short introduction
Clouds consist of adiabatic (undiluted) and non-adiabatic parts. The adiabatic fraction (AF) is a measure of adiabaticity and, hence, of mixing.
The AF is defined as $LWC/LWC_{ad}$, where $LWC_{ad}$ is the liquid water content that a parcel would gain while being lifted adiabatically from the cloud base. [Eytan at el. (2021)](https://acp.copernicus.org/articles/21/16203/2021/acp-21-16203-2021.html) tested different methods to calculate AF values by comparing them to an Eulerain passive tracer. The method found to be the most accurate follows the analytical derivation of [Korolev and Mazin (2003)](https://journals.ametsoc.org/view/journals/atsc/60/24/1520-0469_2003_060_2957_sowvic_2.0.co_2.xml?tab_body=abstract-display) of the supersaturation in an adiabatic ascending parcel while changing the time domain to vertical coordinates (and changing $q_w = \frac{LWC}{\rho_d}$).

 (1)$\frac{dlog(S+1)}{dz}=A_1-A_2\frac{dLWC}{dz}$ 


(2)$A_1=\frac{g}{T}(\frac{L_w}{c_pR_vT}-\frac{1}{R_a})$

(3)$A_2=\frac{1}{\rho_v}+\frac{L_w^2}{c_pR_vT^2\rho_d}$ 

where $S$ is the supersaturation, $g$ is the gravity acceleration, $T$ is the temperature, $L_w$ is the latent heat of water evaporation, $c_p$ is the specific heat of air at constant pressure, $R_v$ and $R_a$ are the specific gas constants of water vapor and dry air, respectively, and  $\rho_v$ and $\rho_d$ are the respective density of water vapor and dry air.
Since these equations do not include mixing effects, we can consider that $LWC = LWC_{ad}$. Additionally, for $S<<1$, Eq.1 can be approximated to


$LWC_{ad}(z)\approx \int_{z_0}^{z'}\frac{A_1(z')}{A_2(z')}dz'-\int_{z_0}^{z}\frac{1}{A_2(z')}\frac{dS}{dz'}dz'$

where $z_0 = 0$ at the cloud base.

