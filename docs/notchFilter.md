# Notch Filter

The EEG data were contaminated by a 60 Hz power line artifact. 
This is a common problem, and a dedicated function to remove such artifacts will come in handy.

Steps: 

1. Create a `./code/upsideDownGaussian.m` function that takes a vector of `frequencies`  and returns a value of 0 for frequencies equal to `trough` and gradually larger values (using `width`) for frequencies far away from `trough`.
1. Create a function `./code/notchFilter.m` that uses `fft`, `ifft`, and your `upsideDownGaussian` to remove power line artifacts.
1. Create a script (`./code/testNotch.m`) that tests your functions on the `./data/eegData.mat` as well as some sample data that you construct by summing a (small number of) sinusoids (including some near 60 Hz).
1. Compare your result with one using `filtfilt` by using a `'bandstopiir'` filter. Use `designfilt` and `fvtool` to understand what such a filter looks like in Fourier space.

