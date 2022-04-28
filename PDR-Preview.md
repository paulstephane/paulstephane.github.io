**It’s been a long time coming…**

 
ECDesigns is a two-person operation run by brothers John and Gordon Brown; John handles circuit design and Gordon oversees the programming aspects. They are based near Eindhoven in the Netherlands, and products are sold directly through their website: www.ecdesigns.nl.


John Brown introduced himself on DIYAudio in 2006 with these words: "I have spent my entire life designing, repairing and building electronic equipment – electronics is my passion..." He started soldering when he was 6, fixing his dad's radio. Does that make him the Mozart of digital audio? That remains to be seen.


ECDesigns’ quest to improve digital audio has led over the years to many product incarnations.


The first product of theirs that convinced me they were doing something different was a small USB disc player, the **UPL**: a battery-operated, low-noise micro-processor playing WAV files on a USB stick with a remote control and a single Toslink output. To be played, files had to be numbered 01-99 in folders numbered 01-99. What made it worth that hassle was the impressive sound quality, a result of the minimalistic design.

![UPL2](https://user-images.githubusercontent.com/33669641/165709060-a84fdf96-8052-4076-a080-24a41602db74.jpg)

After using the UPL I could not go back to other digital music players and have used it since as my main music source. I have often taken it along to audiophile gatherings here in Paris. While many were truly impressed by the UPL's sound quality, the inconvenience of using it meant that very few adopted it. The UPL was also a good benchmark against which other digital sources could be evaluated.

 

ECDesigns’ DAC at the time – the MOS 16 – did not leave as lasting an impression as the UPL did, although it did perform quite well and was priced very reasonably.

 

Fast-forward to 2020, with yet another new DAC – the **DA96ETF**, aka **Fractal DAC**.



![Fractal](https://user-images.githubusercontent.com/33669641/165710879-264b388a-b197-4cb4-bff4-7c2f5e836387.jpg)



On this very forum, a happy few discussed it enthusiastically, offering comparisons with other – often more expensive – DACs.

 

One technical aspect of the DAC that I found interesting (and relatively easy to understand) is key: ECDesigns implemented a mechanism to convert the I2S signal output by the Toslink “decoder” into a parallel signal using a very low bandwidth: 100kHz as opposed to several GHz.

 

Why does that matter? Because lower bandwidth leaves less opportunity for interference to travel along the wiring and circuits.

 

John Brown recently told me: "Designing DACs is similar to designing RF (Radio Frequency) circuits...". And that is as much as I need to know.

 

Shortly after the release of the Fractal DAC, ECDesigns offered to retrofit this “bandwidth limiter” solution to some of the circuits in the UPL. The bandwidth limiter was not as sophisticated (and also less costly) as the one used in the DAC: it limited the bandwidth to 20 MHz from several GHz. ECDesigns sent me a second unit and I was able to compare both: sound quality had further improved, confirming the validity of their approach.  

 

The combination of the revised UPL with the Fractal DAC offered a level of quality in digital playback beyond anything I had heard before.

 
![DA96](https://user-images.githubusercontent.com/33669641/165711289-105da4c8-2891-4a33-a904-662eaaa31887.jpg)


 

Could all this be further improved? Could the same audio quality be obtained from any source? John and Gordon Brown went back, once again, to the drawing board.

 

Their newest product, the PowerDAC-R, builds and improves on these techniques while offering additional features.

 

**The PowerDAC-R**

 



![Rack](https://user-images.githubusercontent.com/33669641/165711543-9c099ee2-24d2-457a-9187-bbaa583c7948.jpg)

 

 

The simple and slightly retro look of the PowerDAC-R appeals to me but may not please everyone. It is surprisingly small but heavy for its size, sitting firmly on its round base. The back of the unit has two RCA analog outputs, a Toslink digital input, and a USB-B plug for the power supply (5v) and firmware updates.

 

ECDesigns sent me three additional accessories to evaluate the PowerDAC-R. These are sold separately:

 

* A self-powered USB to Toslink converter, of their own design
* An RCA to mini-jack adapter cable for connecting headphones to the PowerDAC-R
* A Remote Control for volume control and muting (volume can be controlled otherwise with the pushbuttons on top of the unit)
 

 

![Desktop with comments](https://user-images.githubusercontent.com/33669641/165711798-c8b5f0f4-d11d-47d4-9d01-d6e1614053ba.jpg)




 

The unique internal design is what is worthy of our attention here.

 

The PowerDAC has a single Toslink input (max 24/192kHz) like its predecessor but runs on an independent “master” clock.

 

 

![PowerDAC](https://user-images.githubusercontent.com/33669641/165711589-56098f3a-d5d3-4f4b-9f53-52980d4d93b0.jpg)



 

The method devised to “re-clock” the SPDIF data in the PowerDAC is proprietary:

 

*The incoming digital signal is buffered into a micro-controller’s random-access memory (RAM), sample rate is determined algorithmically, and parallel data is output based on timing provided by a single master clock (asynchronously).*

 

*All data transfers occur at low bandwidth (200kHz). The critical I2S interfaces (high bandwidth, powerful RF noise source) have been completely removed.*

 

The best of both worlds? Perfect galvanic isolation from the source with an optical Toslink input and high-precision re-clocking? ECDesigns claims, as a result, that the DAC should provide high immunity to the quality of the source. This is a bold claim that has been made before.

 

ECDesigns offered me a pre-production model to beta test. I was very eager to see for myself how this PowerDAC performed on that aspect alone and find out what differences, if any, remained between a computer source and my trusted UPL.

 

But wait, there’s more.

 

The PowerDAC includes a novel amplification system with 10 volume levels (+3db each). The PowerDAC-R generates the desired output voltage by the D/A converter itself without using any amplification, buffer or attenuator circuits.

 

ECDesigns has published pictures and technical information about the PowerDAC-R on their website: https://www.ecdesigns.nl/en/blog/rd-powerdac

 

**Listening tests – source immunity**

 

To assess the source immunity of the PowerDAC-R, I compared several sources over a few days using both my speakers and headphones:

 
|Sources|Details|
| ------------- | ------------- |
|UPL96ETL|Low-noise USB key player with WAV files. ElectroTos cable with standard spdif protocol (see here: https://www.ecdesigns.nl/en/blog/upl96etl)|
|RaspberryPi|Model 4B, running Squeezelite, powered by iFi Audio iPower 5V SMPS, network through ethernet port, USB out to ECDesigns’ USB-Toslink converter|
|Intel NUC|NUC5CPYH running Daphile, powered by its standard SMPS, Toslink out from its mini-jack port|
|CD Player|Arcam FJM DV27, Toslink output|

 

I was unable to hear any differences between these sources.

 

So I had a friend over to carry out a “blind test”. I played a well-recorded track that he is very familiar with, using both the RaspberryPi and UPL in the following order: 1) UPL 2) RaspberryPi 3) RaspberryPi 4) UPL. He thought both were excellent and guessed: 1) RaspberryPi 2) UPL 3) UPL 4) RaspberryPi.

 

I have since been exclusively using my Intel NUC connected to the PowerDAC-R using a 1.5m Toslink cable to play music in my living room. It sounds awesome! More about this later…

 

I also tested the PowerDAC-R using a Farad 5-volt power supply and could find no difference in sound quality – this was not the case with the previous DA96ETF DAC. The PowerDAC requires only 200mA of power at 5v. The small linear power supply provided by ECDesigns has a “reservoir capacitance” of 18800uF. The low bandwidth data communication inside the DAC also contributes to power supply “immunity”.

 

**Listening tests – volume control**

 

Output volume can be adjusted using either the remote control or the pushbuttons on the top of the unit. There are 10 (3db) steps, providing a total range of 27db. This translates into a voltage range of 44mV to 1.4 V rms, with a constant output impedance of 31.25 Ohms.

 

The volume control can be deactivated using a jumper on the back of the unit. This results in setting the volume to its highest level (9) and deactivates the pushbuttons and remote control.

 

During my listening tests, the use of the volume control never seemed to deteriorate sound quality.

 

To confirm these impressions, I performed a “Bolero Test” (see here: http://www.high-endaudio.com/RC-Linestages.html#BOLERO ). I used a well-recorded CD that was recorded at low volume. “For Duke” by Billy Berry and His Ellington All-Stars is a Direct to Disc recording of exceptional quality.

 
![ForDuke](https://user-images.githubusercontent.com/33669641/165711630-37d128cc-2813-4124-959e-57ad5345cbab.jpg)

 

My power amplifiers (ECDesigns’ own MBV mono blocks) have three gain settings. At their lowest gain setting and with maximum volume set on the PowerDAC-R (position 9), the volume coming through my speakers was at a comfortable level. I then compared the sound with the amplifiers set at maximum gain while adjusting the PowerDAC-R’s volume control to achieve a similar sound level. I did not compare the levels exactly with a decibel meter and did not feel the need for it, as it was obvious that there was no deterioration in quality even at much lower volumes. The music sounded detailed and distortion-free even at surprisingly low volume levels.

 

Note: the PowerDAC-R provides sufficiently fine volume adjustments (3db steps), but over a fairly narrow range (27db). If the PowerDAC-R is used with amplifiers that are too powerful for your speakers, ECDesigns suggests using fixed shunt attenuators for volume range matching.

 

**Listening tests – headphone use**

 

I tested the PowerDAC-R using two headphones: Grado GH2 and Beyerdynamic DT990 Pro. I used the short RCA to mini-jack adapter that ECDesigns sent me to connect my headphones directly to the PowerDAC-R.

 

The PowerDAC-R was able to drive both headphones effortlessly. The volume range provided sufficient gain to reach a high level. The sound was exceptionally clear, offering a window into the recordings.

 

I also connected the PowerDAC-R (set at max. volume) to my Hagerman Audio Tuba headphone amplifier. The presentation was slightly more “relaxed” - this could be due to some treble roll-off on the Tuba amplifier.

 

ECDesigns have since explained that differences in perceived sound quality between solid-state and tube amplifiers may be due to improved accuracy when driving speaker coils at “constant current” (tubes) rather than “constant voltage” (solid state). Interestingly, they are developing their own tube speaker amplifier to pair with the PowerDAC-R.

 

**Listening tests – comparison with the DA96ETF**

 

Using the UPL as a source, the PowerDAC-R outperforms the previous DA96ETF DAC. There are several reasons for this improved performance:

 

The DA96ETF is dependent on the source’s quality (jitter level). While the UPL, in its latest incarnation, offers a low-jitter signal to the DAC, it is not perfect – no source is.
The DA96ETF decodes the incoming Toslink signal using a standard chip (DIR9001) that outputs I2S – as a result, I2S spectrum cannot be prevented from spreading across the DAC circuit.
The PowerDAC-R has a much lower output impedance (31 Ohm versus 370 Ohm), which improves drive capability.
Some adjustments have been made to the PowerDAC’s “DAC” section, now combining Fractal logic with R2R for lower bits
 

**Overall sound quality of the PowerDAC-R**

 

There is no need for me to wax eloquent here. Listening to the PowerDAC-R really makes me think that I am getting the most out of my digital files, whether they are older recordings or newer releases. No other DAC has given me this impression so unambiguously. Everything sounds “right” – from the tone of individual musicians I am most familiar with to the dynamics of a large ensemble. Moreover, I doubt such quality has ever been offered by a product that is so affordable, so easy to use, and complete in and of itself (no tweaking required).  

 

I now feel I can “check off” the digital aspect of my sound system and focus on making further improvements to the analog side. 
