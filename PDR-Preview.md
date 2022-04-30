*April 2021*

ECdesigns is a two-person operation run by brothers John and Gordon Brown; John handles circuit design and Gordon oversees the programming aspects. They are based near Eindhoven in the Netherlands, and products are sold directly through their website: **[www.ecdesigns.nl](www.ecdesigns.nl)**.


John Brown introduced himself on DIYAudio in 2006 with these words: "I have spent my entire life designing, repairing and building electronic equipment – electronics is my passion..." He started soldering when he was 6, fixing his dad's radio. Does that make him the Mozart of digital audio? That remains to be seen.


ECdesigns’ quest to improve digital audio has led over the years to many product incarnations.


Their newest product, the **PowerDAC-R**, builds and improves on previous products and techniques while offering additional features.

![Rack](https://user-images.githubusercontent.com/33669641/165711543-9c099ee2-24d2-457a-9187-bbaa583c7948.jpg)

 
The simple and slightly retro look of the PowerDAC-R appeals to me but may not please everyone. It is surprisingly small but heavy for its size, sitting firmly on its round base. The back of the unit has two RCA analog outputs, a Toslink digital input, and a USB-B plug for the power supply (5v) and firmware updates.

ECdesigns offered me a pre-production model to beta test. I was very eager to see for myself how this PowerDAC performed on that aspect alone and find out what differences, if any, remained between a basic computer source and dedicated audio sources.

ECdesigns sent me three additional accessories to evaluate the PowerDAC-R. These are sold separately:


* A self-powered USB to Toslink converter, of their own design
* An RCA to mini-jack adapter cable for connecting headphones to the PowerDAC-R
* A Remote Control for volume control and muting (volume can be controlled otherwise with the pushbuttons on top of the unit)





 

![Desktop with comments](https://user-images.githubusercontent.com/33669641/165711798-c8b5f0f4-d11d-47d4-9d01-d6e1614053ba.jpg)

ECdesigns has published pictures and technical information about the PowerDAC-R on their website: https://www.ecdesigns.nl/info/powerdac-r

## 1. Design

The unique internal design is what is worthy of our attention here.Three aspects will be described in detail:

1) Source immunity

2) Fractal DAC architecture

3) Volume control


![PowerDAC](https://user-images.githubusercontent.com/33669641/165711589-56098f3a-d5d3-4f4b-9f53-52980d4d93b0.jpg)



### 1.1 Source Immunity

The PowerDAC has a **single Toslink input** (max 24/192kHz) but runs on an independent “master” clock. The method devised to “re-clock” the SPDIF data in the PowerDAC is proprietary. Here are ECdesigns explantions:


*The PowerDAC-R -only- collects the data from the incoming signal and places it in RAM (Random Access Memory).  Next, the incoming sample rate is measured with a software-based frequency meter. So now the data is available, and the playback rate is determined.*

*Low jitter master clock (Vectron, Pletronics, -85 ... -90dB phase noise @ 10Hz) is used to generate a clean latch signal for the Fractal D/A converter. So we are -not- re-clocking a jittery clock signal and creating said radio transmitter.  We are generating a new, clean clock from scratch that will be used to latch the data (we stored in RAM) into the Fractal D/A converter.*


*The Fractal D/A converter does not work with I2S or other serial data interface and requires no clocks to clock in serial data because there is no serial data. All problems related to high frequency clocks and high frequency serial data are eliminated this way.*


*All bits are presented to the Power D/A converter simultaneously (parallel). Then we wait until all bits are stable and switching noise is completely gone (because the bits no longer change). Now one single latch pulse (derived from the low jitter master clock) will write the new sample to the D/A converter output at the moment there is minimum electrical interference. This helps to minimize trigger uncertainty and provides a clean, low jitter latch signal.*

*In other words, we only have to load new data and latch this data once every sample. The highest frequency we need (data and latch) equals the sample rate (44.1 ... 192 KHz). With conventional DACs we need much higher clock and data rates, typically up to 24.576 MHz. These higher data and clock rates produce much more switching noise and because there is no radio silence during latching, jitter at the D/A conversion circuit will be rather high regardless of master clock phase noise (jitter).*

*The bandwidth we need for getting data into the PowerDAC-R D/A converter is therefore only 192 KHz. This helps to keep most of the source noise that still has to enter through Toslink out of the D/A converter output signal.*

*So what have we achieved with this?*

*1) The single, low frequency latch signal is -completely- independent from the source and because we use professional clocks, phase noise and related jitter is very low (data sheet specifies -85 ... -90 dB phase noise @ 10Hz offset). And that is pretty good.*

*Because the latch frequency is much lower than this master clock frequency, the impact of this phase noise is further reduced, this is not the case with standard DACs that need the native master clock frequency for serial data clocking.*

*2) The large bandwidth noise from the source (bandwidth up to 1 GHz is required to get the data through) is band limited by the optical Toslink interface to approx. 25MHz. This minimizes the noise injection into the D/A converter. Because we can't fully block all noise, marginal source dependency remains but, in most cases, this is so little that it's a non-issue*



The best of both worlds? Perfect galvanic isolation from the source with an optical Toslink input and high-precision re-clocking? ECdesigns claims, as a result, that the DAC should provide high immunity to the quality of the source. This is a bold claim that has been made before.


### 1.2 Fractal DAC Architecture for greater DAC accuracy


The PowerDAC is based on an R2R ladder, but with ECD's own extended "Fractal" solution. I asked John Brown to explain this, and he was kind enough to provide the following illustrations. 


*The Fractal D/A converter is completely different from existing D/A converters as it chops up the most significant bits (the most critical one's for obtaining low bit errors) into tiny fragments. This is what the fractal circuit does. The fragmenting reduces bit errors and glitches. The downside is that we have to use more bits that represent the same bit depth (circuit gets a bit more complicated).*

*An R2R DAC with  16 bits resolution can output 2ˆ16 = 65536 different analogue levels. The bits represent the following values:*

bit0 = 32768

bit1 = 16384

bit2 = 8192

bit3 = 4096

bit4 = 2048

bit5 = 1024

bit6 = 512

bit7 = 256

bit8 = 128

bit9  = 64

bit10 = 32

bit11 = 16

bit12 = 8

bit13 = 4

bit14 = 2

bit15 = 1


*If a DAC outputs 2 Volts, the MSB ("Most Significant Bit" - bit0) would represent 1 Volt. 1 bit error represents 2 / 2ˆ16 = 30 microvolts. So in order to maintain 16 bit accuracy, the MSB voltage would need to be accurate down to at least 30 microvolts and that's very difficult to achieve with any practical circuit. The lower bits bit6 ... bit15 represent much smaller fragments of the output signal and are therefore less critical as an error here has less impact on the output signal.*

 
*The Fractal converter fixes this problem by chopping up the problematic MSBs (bit0 ... bit4) into smaller fragments. The remaining bits can be converted using a R2R ladder.*

*The fractal converter in the PowerDAC-R has 18 bits resolution that represents 262144 levels (auditory system absolute maximum resolution). So we start off with larger numbers:*

fbit1 = 32768

fbit2 = 32768

fbit3 = 32768

fbit4 = 32768

fbit5 = 32768

fbit6 = 32768

fbit7 = 32768

*The remaining bits are converted using R2R ladder:*


bit3 = 16384

bit4 = 8192

bit5 = 4096

bit6 = 2048

bit7 = 1024

bit8 = 512

bit9  = 256

bit10 = 128

bit11 = 64

bit12 = 32

bit13 = 16

bit14 = 8

bit15 = 4

bit16 = 2

bit17 = 1


*We now have a 22 bit fractal converter with 18 bit resolution. The advantage is that the fractal bits have less weight compared to bit0 and bit1 of a comparable R2R ladder DAC (bit0 would represent 131072).  This translates to reduced bit errors and lower glitch (glitch energy reduced from 32768 to 8192 or factor 4).  Another advantage is that we can now obtain 8 times lower output impedance with the same bit switches and resistors as the fractal resistor value is 8 times higher compared to a R2R ladder converter.  With same error introduced by a MOSFET switch (internal resistance RDSon) it will have 8 times less impact on bit accuracy.*



### 1.3 Lossless Volume Control


The PowerDAC includes a novel amplification system with 10 volume levels (+3db each). The PowerDAC-R generates the desired output voltage by the D/A converter itself without using any amplification, buffer or attenuator circuits.

Output volume can be adjusted using either the remote control or the pushbuttons on the top of the unit. There are 10 (3db) steps, providing a total range of 27db. This translates into a voltage range of 44mV to 1.4 V rms, with a constant output impedance of 31.25 Ohms. The powerDAC-R works as an "attenuator" - the current provided by the power supply passes through a series of switches (one per "bit") and resistors that attenuate the current based on the digital signal. This is summarized in the following diagram, and is explained in further detail in their documentation:


![mechanism](https://user-images.githubusercontent.com/33669641/165806464-b6f9171d-4249-481d-a0a9-1b16055ab0c3.JPG)
 

The volume control can be deactivated using a jumper on the back of the unit. This results in setting the volume to its highest level (9) and deactivates the pushbuttons and remote control.



## 2. Listening Tests

### 2.1 Source Immunity

 
To assess the source immunity of the PowerDAC-R, I compared several sources over a few days using both my speakers and headphones:

 
|Sources|Details|
| ------------- | ------------- |
|UPL96ETL|Low-noise USB key player with WAV files. ElectroTos cable with standard spdif protocol ([UPL Documentation](https://www.ecdesigns.nl/00dc/upl96-info.pdf))|
|RaspberryPi|Model 4B, running Squeezelite, powered by iFi Audio iPower 5V SMPS, network through ethernet port, USB out to ECdesigns’ USB-Toslink converter|
|Intel NUC|NUC5CPYH running Daphile, powered by its standard SMPS, Toslink out from its mini-jack port|
|CD Player|Arcam FJM DV27, Toslink output|

 

I was unable to hear any differences between these sources.

 

So I had a friend over to carry out a “blind test”. I played a well-recorded track that he is very familiar with, using both the RaspberryPi and UPL in the following order: 1) UPL 2) RaspberryPi 3) RaspberryPi 4) UPL. He thought both were excellent and guessed: 1) RaspberryPi 2) UPL 3) UPL 4) RaspberryPi.

 

I have since been exclusively using my Intel NUC connected to the PowerDAC-R using a 1.5m Toslink cable to play music in my living room. It sounds awesome! More about this later…


When listening to the PowerDAC-R in others' systems, I always connected their high-end USB sources using ECDesign's own UT96 USB to optical converter.  This small converter is a very basic model that costs only 150€: it does not contain fancy clocks, power regulators, isolation, etc... This is clearly not a piece of equipment one would normally find in a "high-end" digital chain. Yet, during these listening sessions, it never seemed to get in the way. How could that be? I can only conclude that the PowerDAC does correct for the high-level jitter associated with a Toslink connection while benefitting from the Toslink's perfect galvanic isolation from the source. 


I also tested the PowerDAC-R using a Farad 5-volt power supply and could find no difference in sound quality – this was not the case with the previous DA96ETF DAC. The PowerDAC requires only 200mA of power at 5v. The small linear power supply provided by ECdesigns has a “reservoir capacitance” of 18800uF. The low bandwidth data communication inside the DAC also contributes to power supply “immunity”.

 

### 2.2 Volume Control
 

During my listening tests, the use of the volume control never seemed to deteriorate sound quality.


To confirm these impressions, I performed a “Bolero Test” (see here: http://www.high-endaudio.com/RC-Linestages.html#BOLERO ). I used a well-recorded CD that was recorded at low volume. “For Duke” by Billy Berry and His Ellington All-Stars is a Direct to Disc recording of exceptional quality.

 
![ForDuke](https://user-images.githubusercontent.com/33669641/165711630-37d128cc-2813-4124-959e-57ad5345cbab.jpg)

 

My power amplifiers (ECdesigns’ own MBV mono blocks) have three gain settings. At their lowest gain setting and with maximum volume set on the PowerDAC-R (position 9), the volume coming through my speakers was at a comfortable level. I then compared the sound with the amplifiers set at maximum gain while adjusting the PowerDAC-R’s volume control to achieve a similar sound level. I did not compare the levels exactly with a decibel meter and did not feel the need for it, as it was obvious that there was no deterioration in quality even at much lower volumes. The music sounded detailed and distortion-free even at surprisingly low volume levels.

 

Note: the PowerDAC-R provides sufficiently fine volume adjustments (3db steps), but over a fairly narrow range (27db). If the PowerDAC-R is used with amplifiers that are too powerful for your speakers, ECdesigns suggests using fixed shunt attenuators for volume range matching.

 

### 2.3 Headphone and Speaker use
 

I tested the PowerDAC-R using several headphones: Grado GH2, Beyerdynamic DT990 Pro, Etymotic ER4SR, and Sennheiser HD6XX. I used the short RCA to mini-jack adapter that ECdesigns sent me to connect my headphones directly to the PowerDAC-R.

The PowerDAC-R was able to drive these headphones effortlessly. The volume range provided sufficient gain to reach a high level. The sound was exceptionally clear, offering a window into the recordings. I particularly enjoyed the Etymotic and Sennheiser with the powerDAC-R. The Etymotic has an impedance of 45 Ohm, and the Sennheiser 300 Ohm, but with still low sensitivity. The Dan Clark Aeon Noire were too difficult to drive with the powerDAC-R, but they have a much lower sensitivity.

![20220430_144600](https://user-images.githubusercontent.com/33669641/166106230-877d7fe4-0454-4dbc-8bb8-18e09454e0b4.jpg)


With speakers, the powerDAC-R's performance is still very dependent on the rest of the analog system: cables, amplification, speakers. 

I was able to compare the PowerDAC-R to the following DACs in different systems: Audiomat Tempo 2.9, Denafrips Terminator, Rockna Wavelight, Aqua La Voce S3. These comparisons were conducted with other "audiophiles" in their homes. We did not always agree on everything, but it is fair to say that the PowerDAC generated interest and left most impressed. My takeaway from all these tests is simple:  these different DACs have more in common with each other than they do with the PowerDAC. There are several reasons, I believe, for the unique sound quality of the PowerDAC-R.

However, the powerDAC-R used with high quality headphones directly connected to its RCA outputs can already give us today a good idea of what to expect with the future S model and speakers. 

Testing the powerDAC-R with amplification and speakers clearly showed the difference in sound quality from headphone use. Plugging headphones directly to the powerDAC-R provides a sound with a much lower level of distorstion. Of course, the result depend on the quality of the headphones used - each headphones introducing some level of distortion. Surprising results may be obtained with some headphones who’s low-level of distortion were not so obvious with conventional headphone amplifiers.

  

**Conclusions**

 
The PowerDAC may not offer a perfectly transparent signal path - no piece of equipment ever will - but it may very well come closer to that ideal than any other audio system has to date. This minimal signal path is composed of very few components. The analog signal is directly produced from an electrical power source (linear, regulated) going through MOFSET switches and resistors. Nothing more. 


The forthcoming S models will contain a larger number of Fractal bits, extra volume steps with a much higher maximum volume level and lower output impedance. The higher number of Fractal bits will provide even higher accuracy, and the ability to drive speakers directly from the PowerDAC's outputs will eliminate the need for traditional amplification. Exciting times ahead!


