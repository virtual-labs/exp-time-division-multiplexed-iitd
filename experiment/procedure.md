<!DOCTYPE html>
<html lang="en">
<head>

</head>
<body>
    <h2>1. Input Parameters</h2>
    <p>To run the OFDM simulator, please provide the following input parameters:</p>
    <ol>
        <li><strong>Number of OFDM Symbols:</strong> Enter the total number of OFDM symbols to simulate.</li>
        <li><strong>Number of Subcarriers:</strong> Specify how many subcarriers will be used in the OFDM modulation.</li>
        <li><strong>Length of Prefix:</strong> Input the length of the cyclic prefix (in samples) to prevent inter-symbol interference.</li>
        <li><strong>Sampling Frequency (Hz):</strong> Enter the desired sampling frequency for the simulation.</li>
        <li><strong>SNR (dB):</strong> Specify the signal-to-noise ratio for the simulation in decibels.</li>
    </ol> 
    <h2>2. Running the Simulation</h2>
    <p>After entering the parameters, follow these steps:</p>
    <ol>
        <li>Click the <strong>Generate</strong> button to start processing the inputs.</li>
        <li>The simulator will generate the OFDM signal based on the input parameters.</li>
        <li>Observe the generated visualizations, including:</li>
        <ul>
            <li>The time-domain representation of the OFDM signal.</li>
            <li>The frequency-domain representation of the subcarriers.</li>
            <li>BER (Bit Error Rate) vs. SNR graph to analyze performance.</li>
        </ul>
    </ol>  
    <h2>3. Interpreting Results</h2>
    <p>Review the output visualizations:</p>
    <ul>
        <li>Analyze the OFDM signal shape and subcarrier distribution.</li>
        <li>Examine the impact of the cyclic prefix on performance.</li>
        <li>Evaluate the BER vs. SNR graph to understand the system’s robustness under different noise levels.</li>
    </ul>    
    <h2>4. Adjusting Parameters</h2>
    <p>If needed, modify the input values and rerun the simulation to explore different scenarios. This helps in understanding how changes in parameters affect the OFDM signal quality and performance.</p>
</body>
</html>
