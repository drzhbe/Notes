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
* so the common sample rate is 44.1 KHz and the bit-depth of samples is 16 bits
* 1 second of sound: 16 bits sample size * 2 channels * 44.1 KHz sample rate = 176.4 KBytes for 1 second of sound

# Chapter 3: The Frequency Domain

* `A(t) = 2 * Pi * t` amount of angle, that the phasor has gone around at time *t* giving that the frequency is *1 revolution per second* (2 * Pi)
* sine is a `height / radius (sin(A) = a / c)` → `a = c * sin(A)` height of the tip of the arrow relative to the x-axis
* cosine is width / radius (cos(A) = b / c)
* `a = c * sin(A)`, where `a` is a *height* (*h(t)* at the moment *t*) and `c` is a *radius* (and our radius is 1) → `h(t) = 1 * sin(A(t))` (look *A(t)* at the first statement) → `h(t) = sin(2 * Pi * t)`
* So the height is `sin(2 * Pi * t)` and has a graph of curve. To change the curve we can increase *amplitude* (*radius* or *the length of the arrow*) `sin(A) = height / radius` (increasing radius from 1 to 3) → `sin(2 * Pi * t) = h(t) / 3` → `h(t) = 3 * sin(2 * Pi * t)`
* Another way to change the curve is increasing the *frequency* from 1 revolution per second to 5 `A(t) = 5 * (2 * Pi * t) = 10 * Pi * t` → `h(t) = 3 * sin(5 * 2 * Pi * t)`
* So the general formula is `h(t) = Amplitude * sin(Frequency * 2 * Pi * t)`
* The last thing in our graph is the *starting point of the spinning* so we add the *phase shift*, if we want to start the rotation from the angle of *Pi / 4* → `h(t) = 3 * sin(5 * 2 * Pi * t + Pi / 4)`
* The most general formula is `h(t) = Amplitude * sin(Frequency * 2 * Pi * t + PhaseShift)`
* if we make phase shift = 90 degrees, we will get the graph of *cosine*, so the *cosine is phase-shifted sine*
* *angular frequency* `w` (radians / second) related to *frequency* `f` (units / second, Hertz): `w = 2 * Pi * f`
 
## Fourier and the Sum of Sines

* "Any periodic waveform can be expressed as the sum of an infinite set of sine waves" (c) Fourier
* The frequencies of these sine waves must by integer multiples of some fundamental frequency
* To express middle A (440 Hz): 440 Hz, 880 Hz, 1320 Hz...
* Triangle waves only contain partials at odd multiples of fundamental
* @TODO add phasor definition
* @TODO add FFT definition
