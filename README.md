# candlestick-mic

Repairing and retrofitting an old candlestick phone to be used as a headset.

I only did this because I just wanted to hear what it would sound like in Discord.

TODO: picture of phone

## Circuit

TODO: picture of circuit

## Project Summary

A brief summary of what I did in this project.

### How the Phone Works

I jumped into this not knowing anything really. So I had to figure out how the phone worked on a basic level.

To start the research, I think I have what is referred to as a Kellogg No 64 Candlestick (according to [this telephone collecting site](http://www.telephonecollecting.org/Bobs%20phones/Pages/Kellogg/KelloggPhones.htm)). My phone also came with an oak box [magneto](https://en.wikipedia.org/wiki/Telephone_magneto), but I won't be using it for now.

Phones of this era used a [carbon microphone](https://en.wikipedia.org/wiki/Carbon_microphone). 
I found a couple good resources for learning how these work:

- [How to Build a Simple Carbon Microphone](https://www.youtube.com/watch?v=XiAzdxDpwJY)
- [The Boys' First Book of Radio and Electronics (1954) pages 200-202](https://worldradiohistory.com/BOOKSHELF-ARH/Technology/The-Boy%27s-First-Book-of-Radio-Morgan-1954.pdf)
- [Principles of Electricity Applied to Telephone and Telegraph Work (1938) pages 66-68](https://www.amazon.com/Principles-Electricity-Applied-Telephone-Telegraph/dp/B000Q75WQE) - A VERY in depth book about telegraphy and telephony of this era.

For determining what the rest of the phone was supposed to do, I primarily used [telephonecollectors.info](https://www.telephonecollectors.info/strombergcarlson/kellogg/kellogg_main.htm).
Here is a list of old resources I got to skim through:

- [Kellogg Patent Collection 1890-1916](https://www.telephonecollectors.info/strombergcarlson/kellogg/PDF/PATENTS_KELLOGG_ASSIGN.pdf)
- [Kellogg Bulletin 8 - Magneto Telephones 1903](https://www.telephonecollectors.info/strombergcarlson/kellogg/PDF/1903_BLTN_8_MAG_TEL_SETS.pdf)
- [Kellogg Bulletin 38 - Magneto Telephones 1909](https://www.telephonecollectors.info/strombergcarlson/kellogg/PDF/1909_BLTN_38_MAG_TEL_SETS.pdf)
- [Transmitter Wiring #229](docs/229c_tl.pdf) and [Transmitter Wiring #323](docs/323_tl.pdf).
- [Kellogg Wiring Diagrams](https://www.telephonecollectors.info/strombergcarlson/kellogg/PDF/DIAGRAMS.pdf)
- [Telephone Archive - Kellogg](http://www.telephonearchive.com/phones/index.html)
- Supply voltage ended up being two of these [1.5v dry cells]((https://collection.maas.museum/object/214017) in series. I ended up bumping it up to 3.3v

I also downloaded the resources I used and put them in [docs/](docs/) so they never get lost if that site goes down.

### Repairing

Surprisingly, the only thing I really had to repair was a few broken solder joints in the receiver and transmitter. 
I was able to fairly quickly supply voltage and see my voice show up on my oscilloscope...albeit as a very low signal.

### The Rest

For some reason I thought I was going to need to build some DAC (digital to analog conversion) and ADC (analog to digital conversion) circuits to get this working.
So, I found the following resources:

- https://wiki.analog.com/university/courses/electronics/text/chapter-20
- [Digital Audio Fundamentals](https://www.youtube.com/playlist?list=PLbqhA-NKGP6B6V_AiS-jbvSzdd7nbwwCw)

But duh, of course a computer's sound card/front panel take care of converting signals for you.

Since the phone signal was so low, that calls for an amplifier. I'm still an electronics beginner so I used [this page](https://www.circuitbasics.com/build-a-great-sounding-audio-amplifier-with-bass-boost-from-the-lm386/) as a basis, which uses an [LM386 Low Voltage Audio Power Amplifier](https://www.ti.com/lit/ds/symlink/lm386.pdf).

After implementing that, I just had to play around with various capacitors to eliminate additional noise that was causing insane buzzing/humming.
Again, I don't know what I'm doing so I just did trial and error.

To finish the project I finalized my circuit, soldered it to protoboard, and designed/3D printed an enclosure.

## References

Listed above in individual sections.

