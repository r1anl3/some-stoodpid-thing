#Ôn tập Thiết kế mạng
- **Chương 1**
    - OSI model: 7 tầng
        - Segment: A single network bounded by a switch or router and based on a particular Layer 1 and Layer 2 protocol such as Fast Ethernet.
        - LAN: A set of switched segments based on a particular Layer 2 protocol such as Fast Ethernet and an interswitch trunking protocol such as the IEEE 802.1Q standard.
        - Building network: Multiple LANs within a building, usually connected to a building backbone network.
        - Campus network: Multiple buildings within a local geographical area (within a few miles), usually connected to a campus-backbone network.


    - SDLC: 
        - Plan:  Network requirements are identified in this phase. This phase also includes an analysis of areas where the network will be installed and an identification of users who will require network services.
        - Design: In this phase, the network designers accomplish the bulk of the logical and physical design, according to requirements gathered during the plan phase.
        - Implement: After the design has been approved, implementation begins. The network is built according to the design specifications. Implementation also serves to verify the design.
        -  Operate: Operation is the final test of the effectiveness of the design. The network is monitored during this phase for performance problems and any faults to provide input into the optimize phase of the network life cycle.
        - Optimize:  The optimize phase may lead to a network redesign if too many problems arise because of design errors or as network performance degrades over time as actual use and capabilities diverge. Redesign can also be required when requirements change significantly
        - Retire: When the network, or a part of the network, is out-of-date, it might be taken out of production. Although Retire is not incorporated into the name of the life cycle(PDIOO), it is nonetheless an important phase. The retire phase wraps around to the plan phase. The PDIOO life cycle repeats as network requirements evolve.
- **Chương 2**
    - Tính sẵn sàng: `Availability = MTBF / (MTBF + MTTR)`
    - Giải thích ký hiệu:
        - MTBF: mean time between failure/thời gian không lỗi
        - MTTR: mean time to repair/thời gian sửa lỗi
    - Đánh giá hiệu năng:
        - Capacity(bandwith): khả năng truyền dữ liệu, tính bằng bps.
        - Utilization(khả năng sử dụng): phần trăm **capacity** được đang sử dụng.
        - Optimum ultilization(khả năng sử dụng tối đa): trung bình lớn nhất của **utilization**.
        - Throughput(thông lượng): lượng data truyền đi không lỗi trong khoảng thời gian.
        - Offered load: tổng data của các node trong mạng.
        - Accuracy: độ chính xác, liên quan tới các traffic.
        - Efficiency: độ hiệu quả
        ...
    - Bốn nguồn gây trễ gói tin:
        $d_{nodal} = d_{proc} + d_{queue} + d_{trans} + d_{prop} $
        - $d_{proc}$: xử lí tại nút
        - $d_{queue}$: xếp hàng
        - $d_{trans}$: truyền, 
            $d_{trans} = \text{chiều dài gói tin(bits) / băng thông liên kết(bps)}$
        - $d_{prop}$: lan truyền,
            $d_{prop} = \text{độ dài đường liên kết vật lí(m)/tốc độ lan truyền(m/s)}$
        - Queuing delay and bandwidth utilization:
            `queue depth = utilization/(1-utilization)`
            Ex:  A packet switch has **five** users, each offering packets at a rate of **10 bps**. The average length of the packets is **1024 bits**. The packet switch needs to transmit this data over a **56-kbps** WAN circuit.
            - Load = 5 x 10 x 1024 = 51,200 bps.
            - Utilization = 51,200/56,000 = 91.4%
            - Avg packets in queue = (0.914)/(1-0.914) = 10.63 packets