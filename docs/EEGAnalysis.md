# EEG Analysis

Following the examples in `./docs/spectralAnalysis.mlx`, perform a spectral analysis of the EEG data set (`./data/eegData.mat`).

Steps:
1. For each channel, calculate the amplitude spectrum (note that fft is vectorized, so make use of this feature)
1. To determine the frequency axis you need to calculate the sample rate from the `eegTime` vector
1. Many natural signals, including those in the brain, have a so-called 1/f spectrum ("one over f"). 
    This means that the power drops as the frequency increases. As a consequence, a plot of an amplitude spectrum 
    is often dominated by low frequencies even when there is interesting stuff happening at the higher frequencies. 
    Correct this by using a log-scale on the amplitude axis. You should do this by changing the plot, not the data!
1. Plot each channel in a separate subplot and use `title` to identify the channel. Don't duplicate code; use a loop.
1. What are some dominant frequencies in this EEG recording? Can you interpret them? 
1. Why are there so many conspicuous downward peaks in the spectra?

Add structured code and comments to `/code/eegAnalysis.m` for each of these steps. Use proper styling.
