# Fourier transforms for real signals. 

Because Neuroscientist rarely use complex signals, it is easier to have an FFT function that deals just with real signals. Moreover, extracting the correct frequencies for the FFT can be tricky and it is not something you want to deal with every time you do an FFT. Because this is such a generic operation that you may use many times in your analyses, it is a perfect candidate for a function in your own toolbox. Create a function called `fftReal.m` that takes two inputs: the data and the sampling rate and returns the first half of the Fourier spectrum together with the frequencies for each of the components:

Then, create the matching `[signal,time] =ifftReal(comps,freqs)` that takes the output of `fftReal` and transforms it back into the time domain.

All the code needed to do this is available in the example scripts of this module; you only have to package this into a function (and add error checking, and proper documentation!).
