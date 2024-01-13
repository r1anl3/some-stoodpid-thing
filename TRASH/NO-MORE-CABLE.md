#Ôn tập hệ thống nhúng
- Fundamentals in wireless transmissions {20%}
    - **Nyquist Bandwidth**
        - Đường truyền **không nhiễu**. 
        - $\begin{cases} 
        C = 2B \text{(băng thông max)} \\
        C = 2B\log_2M \text{(nhiều mức tín hiệu)}
        \end{cases}$
        - Explain symbols:
            - $B$: băng thông/bandwidth(**Hz**)
            - $C$: tốc độ truyền/capacity(**bps**)
            - $M$: số mức tín hiệu/numbers of discete signal/votage levels(**không đơn vị**)
    - **Signal-to-Noise Ratio(SNR)** 
        - **Tỉ lệ** giữa cường độ tín hiệu(signal power) và cường độ nhiễu(noise power)
        - Quy đổi đơn vị($db$): $(SNR)_{db} = 10\log_{10} \frac{\text{signal power}}{\text{noise power}} = 10\log_{10}SNR$
    - **Shannon Capacity**
        - Đường truyền **có nhiễu**
        - $C = B\log_2(1 + SNR)$
        - $SNR\text{ không tính đơn vị}$
    - **Antena Gain**
        - Tín hiệu ăng-ten nhận được ở trong khu vực ảnh hưởng
        - $G = \frac{4\pi A_e}{\lambda^2}= \frac{4\pi f^2 A_e}{c^2}$
        - Giải thích ký hiệu
            - $G$: tín hiệu nhận/attena gain (không đơn vị)
            - $A_e$: diện tích khu vực ảnh hưởng/effective area ($m^2$)
            - $f$: tầng số sóng mang/carrier frequency (Hz)
            - $c$: tốc độ ánh sáng/speed of light ($3*10^8 \ m/s$)
            - $\lambda$: bước sóng sóng mang/carrier waveleght (m)
        - Chuyển về db: $10\log_{10}(G)$
    - **Light-of-Sight Propagation**
        - Truyền tín hiệu theo đường thẳng
        - $LOS = 3.57(\sqrt{Kh_1} + \ \sqrt{Kh_2}) $
        - $\begin{cases}
        d = 3.57\sqrt{h}(\text{Optical line of sight} ) \\
        d = 3.57\sqrt{Kh}(\text{Effective, or radio, line of sight} ) \\
        \end{cases} $
        - Giải thích ký hiệu
            - $d$: khoảng cách giữa 2 ăng-ten (km)
            - $h$: độ cao của ăng-ten (m?)
            - $K$: thường là 4/3
    - **Free Space Loss**
        - Suy hao trong không gian
        - **Tỉ lệ**
        - $\frac{P_t}{P_r} = \frac{(4\pi d)^2}{(\lambda)^2} = \frac{(4\pi f d)^2}{c^2}$
        - Giải thích ký hiệu
            - $Pt$ = cường độ tín hiệu ăng-ten truyền/transmit 
            - $Pr$ = signal power at receiving antenna
            - $\lambda$ = carrier wavelength
            - $d$ = propagation distance between antennas
            - $c$ = speed of light ($3 * 10^8$ m/s)
            - where $d$ and $\lambda$ are in the same units (e.g., meters)
    ...

        
- Technologies for different scenarios/applications {wifi}, comparisons of network technologies  20%

- Flows of operations [linux network kernel, drivers, packet transmission, packet reception/forwarding]    40%

- Alternative questions {projects} 20%