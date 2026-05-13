# _I2C_analysis

### Project Description
1) Wire two Raspberry Pi Pico 2 boards on a shared breadboard, with one acting as I2C master driving an OLED display and the other passively sniffing the SDA and SCL lines
2) Sniffer firmware detects START/STOP conditions, samples bits on SCL rising edges, assembles bytes, decodes address vs data, and identifies ACK/NACK responses
3) Decoded transactions are streamed over USB serial to a host-side Python program that buffers, pretty-prints, filters, and searches the data stream
4) Intended extensions:
   - Extend the master to transmit a "Hello World" string and real sensor data over I2C, capture both with the sniffer, and perform analysis on the buffered output
   - ASCII translation
   - Pattern matching/ data reconstruction
   - Data parsing
