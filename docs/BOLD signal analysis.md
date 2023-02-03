# BOLD Signal Analysis

The signal analysis of `.\data\boldData.mat` in `.\docs\spectralAnalysis.mlx` shows that the voxel follows the time course of the visual paradigm, but how do we know that it responds to Faces or Houses? To assess this you will transform the dominant components back into the time domain using the inverse Fourier Transform.  Note that some of these steps have already been done in the example code.

Steps: 
1. Determine the full set of Fourier components of the bold signal.
1. To get familiar with ifft use it on the Fourier components to get back the time-domain signal. Convince yourself that the back and forth transformation to Fourier space and back is lossless.
1. Set the Fourier component that corresponds to the sum of the signal to zero, and do the iift again. Plot the signal and compare it to the original.
1. Find the dominant frequency in the Fourier spectrum and its two neighbors. (Programmatically! This has to work for any signal, not just this particular example...)
1. Set all Fourier components to zero except those at the dominant frequency and its two neighbors.
1. Use the ifft function to transform these dominant components back into the time domain. If the result contains complex numbers then you should think again about the location of the components below `nyquistIx` and above. You cannot ignore Matlab warnings about complex numbers (i.e.eventually you should receive none when you run your code, and using `real` or `abs` to simply remove the complex numbers is a really bad idea!)
1. Graphically compare this dominant BOLD signal to the real BOLD signal, as well as the time course of the paradigm.
1/ In words, explain how the phase of the dominant signal is related to the lag of the hemodynamic response function (qualitatively!).

Create cell sections (%%) in `.code\boldAnalysis.m` that reflect these steps, commit and push to GitHub for review.
