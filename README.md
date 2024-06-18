###                     Matched Filters, Correlators, ISI, and raised cosine filters 
## System Description
![image](https://github.com/faatthy/Matched-Filters-Correlators-ISI-and-raised-cosine-filters-/assets/110846097/5eb77bbc-af9d-4b2b-8ecf-0d95590ae9e6)

## Matched filters and correlators in noise-free 
environment 
To simulate a binary PAM signaling system, we start by generating 10 random binary bits. These bits 
are then converted into PAM symbols, where logic 1 becomes +1 and logic 0 becomes -1. The symbol 
duration is 1 second. 
To represent the pulse shaping function discreetly, we use 5 samples equally spaced, with a difference 
of 200 ms between each sample. This pulse shaping function is normalized to ensure that its energy is 
unity. 
- Matched and Unmatched filters Ouputs
![image](https://github.com/faatthy/Matched-Filters-Correlators-ISI-and-raised-cosine-filters-/assets/110846097/d4baee25-a6c1-4a03-b381-12f9f608d38a)

- Correlator Output
![image](https://github.com/faatthy/Matched-Filters-Correlators-ISI-and-raised-cosine-filters-/assets/110846097/18a7e269-636a-4933-95fe-07b79251391c)

## Requirement 2: Noise Analysis
The process involves expanding the initial bit sequence of 10,000 bits, generating Gaussian noise with 
zero mean and unity variance matching the size of the sequence. This noise is then scaled to achieve a 
variance of N0/2. It's added to the transmitted sequence, and the resulting signal is filtered using a 
matched filter or a rect filter and sampled. The probability of error is calculated based on a 10,000
sample array. Additionally, N0 is adjusted iteratively to vary Eb/N0 from -2 dB to 5 dB in 1 dB steps, 
with the BER calculated at each step

![image](https://github.com/faatthy/Matched-Filters-Correlators-ISI-and-raised-cosine-filters-/assets/110846097/30b58c45-d9ec-46de-8ef4-f8c96f2c78e5)

## Requirement 3: ISI and raised cosine 
To illustrate the impact of Inter-Symbol Interference (ISI), we employ a noise-free system characterized 
by square root raised cosine filters for both transmission and reception. The raised cosine filter is 
chosen due to its ability to meet the Nyquist criterion, ensuring efficient data transmission by 
minimizing ISI. Although the ideal square root raised cosine filter is theoretically optimal, its infinite 
impulse response renders it impractical for real-world applications. Thus, we utilize a parameterized 
approach to define the practical length of the filter, represented by the delay parameter fig [9], and 
control the filter's bandwidth using the Rolloff factor, denoted as R. By employing square root raised 
cosine (SRRC) filtering at both ends, we aim to approximate the response of a raised cosine filter. This 
ensures that the resultant system exhibits the desired characteristics, facilitating a clearer 
understanding of ISI through the visualization of eye patterns, which graphically represent the received 
signal's characteristics over time. 
![image](https://github.com/faatthy/Matched-Filters-Correlators-ISI-and-raised-cosine-filters-/assets/110846097/2da60959-da80-4c83-8577-5e0c828827c8)
![image](https://github.com/faatthy/Matched-Filters-Correlators-ISI-and-raised-cosine-filters-/assets/110846097/d85aee72-6283-47af-b02e-2230d69beda1)


