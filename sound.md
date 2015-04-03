[Music and computers](http://music.columbia.edu/cmc/musicandcomputers/)
# Chapter 1. The Digital Representation of Sound, Part One: Sound and Timbre

## Physical / Psychophysical
* Frequency / Pitch
* Amplitude / Loudness

## Frequency
* F = repeats/second (Hz)
* Human ear can recognize the following frequencies: 20 Hz – 20 KHz
 
## Period
P = seconds/repeats
 
## Wavelength
W = `sonic speed (345 meters/second)` * `Period`

## Octave 2:1
* 20 Hz – 40 Hz
* 40 Hz – 80 Hz
* 80 Hz – 160 Hz
* ...

## A
55Hz, 110Hz, 220Hz, 440Hz, ...

## Fletcher-Munson Curves
Loudness of 50 Hz tone at 55 dB == loudness of 1000 Hz at 20 dB

# Chapter 2: The Digital Representation of Sound, Part Two: Playing by the Numbers

* ADC analog to digital converter – sound to samples
* DAC digital to analog converter – back to sound
* Analog is continuous, digital is discrete
* *Nyquist sampling theorem:* The sampling rate should be at least twice the highest frequency contained in the sound of the signal
* → as human ear could understand sound up to 20 KHz, sample rate should be at least 40 KHz. But for some reasons it is common to use 44.1 KHz (22.05 KHz as base)
* piano's highest sound is 4 KHz. Frequencies from 4KHz to 20KHz represent timbral, spectral.
* alias could happen when frequency is higher than Nyquist rate
* anti-alias filter will cut-off everything above Nyquist rate (44.1 KHz)
* 
