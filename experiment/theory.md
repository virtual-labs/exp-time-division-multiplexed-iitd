<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body>
    <!-- sidebar and body -->
    <div class="flex min-h-[380px]">
      <div class="maincontent px-8 pb-6 flex-1">
        <div
          class="w-full text-[19.2px] text-[#313636]"
          style="font-family: Raleway, sans-serif"
        >
          <h3 class="text-[24px] font-semibold text-black">
            Orthogonal Frequency Division Multiplexing
          </h3>
          <p>
            When a signal with high bandwidth traverses through a medium, it
            tends to disperse more compared to a signal with lower bandwidth.
            <br />
            <br />
            A high-bandwidth signal comprises a wide range of frequency
            components. Each frequency component may interact differently with
            the transmission medium due to factors such as attenuation,
            dispersion, and distortion. OFDM combats the high-bandwidth
            frequency selective channel by dividing the original signal into
            multiple orthogonal multiplexed narrowband signals. In this way it,
            overcomes the inter-symbol interferences (ISI) issue.
          </p>
          <div class="flex justify-center">
            <img src="./images/theory/ofdm/ofdm1.png" alt="ofdm_image" />
          </div>
          <p>
            OFDM converts frequency-selective channel to multiple (M)
            frequency-flat channels.
          </p>
          <h3 class="text-[24px] font-semibold text-black py-2">
            Block Diagram:
          </h3>
          <div class="flex flex-col justify-center items-center">
            <img src="./images/theory/ofdm/ofdm2.png" alt="ofdm_image" />
            <p class="font-semibold">Fig: OFDM</p>
          </div>
          <p>
            <br />
            In OFDM, modulation and demodulation are performed using IFFT and
            FFT.
            <br />
            <br />
          </p>
          <p class="font-semibold">
            At transmitter side: <br />
            <br />
          </p>
          <div class="flex">
            <img src="./images/theory/ofdm/ofdm3.png" alt="ofdm_image" />
          </div>
          <p class="font-semibold">
            <br />
            At receiver side: <br />
            <br />
          </p>
          <div class="flex">
            <img src="./images/theory/ofdm/ofdm4.png" alt="ofdm_image" />
          </div>
          <p>
            <br />
            In OFDM, Information is signalled in the frequency domain. It is
            based on 1-D transform in frequency domain (IFFT/FFT). Orthogonality
            among the subcarriers is the key.
          </p>
          <div class="flex justify-center">
            <img src="./images/theory/ofdm/ofdm5.png" alt="ofdm_image" />
          </div>
          <h3 class="text-[28px] font-semibold text-black py-2">
            <br />
            Effect of high Doppler in OFDM
          </h3>
          <p>
            In presence of high Doppler, subcarriers lose orthogonality. This
            results in inter-carrier interference (ICI).
          </p>
          <div class="flex justify-center">
            <img src="./images/theory/ofdm/ofdm6.png" alt="ofdm_image" />
          </div>
          <p>
            <br />
            Causes severe degradation in bit error performance for high Doppler
            (error floors). Channel estimation and equalization in high Doppler
            channels is difficult. <br />
            <br />
            To avoid ISI while transmitting many parallel low bandwidth signals,
            the individual subcarriers must be orthogonal to each other.
            Avoiding ISI by transmitting many orthogonal low bandwidth
            subcarriers motivates OFDM. An OFDM modulator converts a high-rate
            serial stream of symbols into many parallel low-rate streams. Each
            orthogonal low-rate stream encounters a relatively flat channel with
            minimal ISI, and can be easily equalized. <br />
            <br />
            To demonstrate, consider a pulse of duration Tsym=0.25 sec, a symbol
            data rate Rsym=1 / Tsym=8 Hz, and additional pulses translated in
            frequency by Rsym, 2Rsym, and 3Rsym. The frequency-translated pulses
            are called subcarriers. <br />
            <br />
            Rsym is the symbol rate of each of the low-rate QAM streams <br />
            Tsym=1 / Rsym (Tsym is the pulse duration of each <br />
            <br />
            An OFDM modulator sums all these subcarriers together to form its
            output signal. Here, the subcarriers are baseband modulated using
            the QAM-method. Mathematically, the sampled modulator output signal
            s(k) is given by <br />
          </p>
          <div class="flex justify-center">
            <img src="./images/theory/ofdm/ofdm7.png" alt="ofdm_image" />
          </div>
          <p>
            Where, am,n is QAM symbol stream and it is a QAM-modulated symbol of
            the mth subcarrier in the nth OFDM time symbol <br />
            <br />
            ‘k’ indicates kth position in a input symbol <br />
            N is the number of subcarriers <br />
          </p>
          <h3 class="text-[28px] font-semibold text-black py-2">
            <br />
            OFDM Transmitter <br />
          </h3>
          <div class="flex justify-center">
            <img src="./images/theory/ofdm/ofdm8.png" alt="ofdm_image" />
          </div>
          <p>
            <span class="font-semibold">1. Data Encoding:</span>Convert the
            input data stream into symbols suitable for transmission (e.g.,
            using QAM, PSK, or other modulation schemes).
            <br />
            <span class="font-semibold">2. Serial-to-Parallel Conversion:</span>
            Group the symbols into blocks, and then convert these serially
            arranged symbols into parallel data streams, one for each
            subcarrier.
            <br />
            <span class="font-semibold"
              >3. IFFT (Inverse Fast Fourier Transform):</span
            >
            Apply the IFFT algorithm to convert the time-domain parallel data
            streams into frequency-domain OFDM symbols. The IFFT operation
            converts the data from the frequency domain to the time domain.
            <br />
            <span class="font-semibold">4. Cyclic Prefix Addition:</span> Add a
            cyclic prefix to each OFDM symbol to mitigate the effects of
            multipath delay spread. The cyclic prefix is a copy of the end part
            of the OFDM symbol that is appended at its beginning. <br />
            <span class="font-semibold">5. Digital-to-Analog Conversion:</span>
            Convert the time-domain OFDM symbols into analog signals. <br />
            <span class="font-semibold">6. Upconversion and Transmission:</span>
            Upconvert the analog OFDM signal to the desired carrier frequency
            and transmit it over the wireless channel.
          </p>
          <h3 class="text-[28px] font-semibold text-black py-2">
            <br />
            OFDM Receiver <br />
          </h3>
          <div class="flex justify-center">
            <img src="./images/theory/ofdm/ofdm9.png" alt="ofdm_image" />
          </div>
          <p>
            <span class="font-semibold">1. Signal Reception:</span>Receive the
            transmitted OFDM signal after it has traveled through the wireless
            channel.
            <br />
            <span class="font-semibold">2. Downconversion:</span>Downconvert the
            received signal to baseband or an intermediate frequency.
            <br />
            <span class="font-semibold">3. Analog-to-Digital Conversion:</span>
            : Convert the analog signal into a digital form suitable for
            processing. <br />
            <span class="font-semibold">4. Cyclic Prefix Removal:</span> Remove
            the cyclic prefix from each OFDM symbol. <br />
            <span class="font-semibold">5. FFT (Fast Fourier Transform): </span>
            Apply the FFT algorithm to convert the time-domain OFDM symbols back
            into the frequency domain. The FFT operation recovers the original
            frequency-domain OFDM symbols.<br />
            <span class="font-semibold">6. Parallel-to-Serial Conversion:</span>
            Convert the frequency-domain symbols back into a serial data stream.
            <br />
            <span class="font-semibold">7. Data Demodulation:</span> :
            Demodulate the received symbols to recover the original data stream.
            <br />
            <span class="font-semibold">8. Channel Equalization:</span> Apply
            channel equalization techniques to mitigate the effects of channel
            impairments, such as frequency-selective fading. <br />
            <span class="font-semibold">9. Data Decoding: </span> Decode the
            received symbols to obtain the original transmitted data. <br />
          </p>
          <!--  -->
        </div>
      </div>
    </div>
</body>
</html>
