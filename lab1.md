Part 1: Capturing HTTP Traffic.

Task 1: Start Wireshark and capture packets.
Step 1: Open Wireshark.
<img width="1918" height="1006" alt="image" src="https://github.com/user-attachments/assets/494bc916-4084-4236-8c43-d3963d36c218" />
Step 2: Select the network interface connected to the internet (e.g., Ethernet or Wi-Fi).
<img width="1919" height="780" alt="image" src="https://github.com/user-attachments/assets/d9a9e616-94e0-4d87-9f7e-3a4aaeb5474e" />
Step 3: Click the "Start Capturing Packets" button (the shark fin icon).
<img width="1412" height="558" alt="image" src="https://github.com/user-attachments/assets/8601dd60-9038-48e7-b2fb-b19a63c3acd4" />
Step 4: Open your favorite web browser and navigate to (http://neverssl.com/) website.
<img width="1919" height="936" alt="image" src="https://github.com/user-attachments/assets/88b5cbda-2e3a-44b3-91e1-0e4666bbb7d8" />
Step 5: After the website has fully loaded, stop capturing packets by clicking the red stop button in
Wireshark
<img width="1919" height="662" alt="image" src="https://github.com/user-attachments/assets/9276d47e-7091-4d72-b5e0-6c99615689ec" />

Task 2: Filter HTTP packets and analyze them.
Step 1: In the filter bar, type http and press Enter. This filters out only the HTTP packets from the capture.
<img width="1919" height="936" alt="image" src="https://github.com/user-attachments/assets/94320974-09b3-42f1-96cb-304cb58505b1" />
Step 2: Select any HTTP packet to view its details.
<img width="1919" height="940" alt="image" src="https://github.com/user-attachments/assets/a0a2f152-d42e-43aa-82e7-b3efc7c576d2" />
<img width="1918" height="973" alt="image" src="https://github.com/user-attachments/assets/a076df81-c3e0-49fc-aaba-f11a7e5a178c" />
<img width="1919" height="966" alt="image" src="https://github.com/user-attachments/assets/b515b8c9-b46a-4f39-bcc4-b94863342a82" />
<img width="1919" height="894" alt="image" src="https://github.com/user-attachments/assets/f19de019-8217-4129-900d-a401df9b609c" />
<img width="1919" height="972" alt="image" src="https://github.com/user-attachments/assets/e94c5d8e-70e1-4b80-8310-21ac49403c19" />
<img width="1919" height="971" alt="image" src="https://github.com/user-attachments/assets/a9f2dd4e-bee7-4dc6-8f27-0ce634ab7b70" />
Step 3: Observe the HTTP request and response messages. Note the method (GET, POST), URL, response codes (200 OK, 404 Not Found), etc.
<img width="1538" height="191" alt="image" src="https://github.com/user-attachments/assets/c8aef892-c366-44e3-9bc0-f1243fd34602" />


Part 2: Analyzing TCP/IP Traffic.

Task 1: Filter TCP packets
Step 1: Clear the previous filter and type TCP to focus on TCP packets.
<img width="1919" height="969" alt="image" src="https://github.com/user-attachments/assets/e50ed33d-8680-4d4d-96cd-0fb6d9ff2d51" />
Step 2: Select a TCP packet related to your HTTP request/response.
<img width="1917" height="968" alt="image" src="https://github.com/user-attachments/assets/d738cd4e-ef2b-48bd-8746-db8f78e1d692" />
Step 3: Right-click on the packet and select "Follow" -> "TCP Stream".
<img width="1919" height="975" alt="image" src="https://github.com/user-attachments/assets/4b4646c1-cd6b-40d9-bfc3-1aeb0df81f3b" />
Step 4: This shows the entire conversation between the client and server.
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/33e00afb-4394-4ae4-b386-c1b5d066f387" />


Task 2: Analyze TCP handshake and investigate Data Transfer and Termination
Step 1: Find and select packets related to the TCP three-way handshake:
o SYN: Initiates a connection.
<img width="1918" height="540" alt="image" src="https://github.com/user-attachments/assets/7a528084-b46a-4d5d-90b5-324286ae3540" />
o SYN-ACK: Acknowledges and responds to the SYN.
<img width="1919" height="581" alt="image" src="https://github.com/user-attachments/assets/fb8fce29-1e30-4c63-b882-eae744a50cbd" />
o ACK: Acknowledges the SYN-ACK and establishes the connection.
<img width="1919" height="568" alt="image" src="https://github.com/user-attachments/assets/d7914873-67dc-4bb4-9f8c-28443981d013" />
Step 2: Note the sequence and acknowledgment numbers. Screenshot and upload your image to your online git repository.
<img width="1918" height="540" alt="image" src="https://github.com/user-attachments/assets/7a528084-b46a-4d5d-90b5-324286ae3540" />
<img width="1919" height="581" alt="image" src="https://github.com/user-attachments/assets/fb8fce29-1e30-4c63-b882-eae744a50cbd" />
<img width="1919" height="568" alt="image" src="https://github.com/user-attachments/assets/d7914873-67dc-4bb4-9f8c-28443981d013" />
| Packet | Source | Seq | Ack | Flags   |
| ------ | ------ | --- | --- | ------- |
| 68     | Client | 0   | -   | SYN     |
| 80     | Server | 0   | 1   | SYN-ACK |
| 81     | Client | 1   | 1   | ACK     |
Step 3: Observe the data packets exchanged between the client and server. Take a screenshot and upload it to your online git repo.
<img width="1918" height="778" alt="image" src="https://github.com/user-attachments/assets/76d09cc5-a205-49e7-870a-2581c69180a6" />
<img width="1919" height="535" alt="image" src="https://github.com/user-attachments/assets/929276a4-3298-441a-95f2-517297008a2c" />
<img width="1918" height="428" alt="image" src="https://github.com/user-attachments/assets/2f42c129-967f-4472-b3dd-f07bcb2c9bc1" />
<img width="1918" height="563" alt="image" src="https://github.com/user-attachments/assets/c1e24b0c-e732-4e9c-93a8-91e4f4df1d4a" />
Step 4: Look at the TCP termination process (FIN, ACK packets).
<img width="1919" height="635" alt="image" src="https://github.com/user-attachments/assets/74a617cc-cc59-4be8-b985-9116556dd6e0" />


Part 3: Capturing and Analyzing UDP Traffic

Task 1: Generate UDP traffic and capture packets
Step 1: Open a network application that uses UDP (e.g., streaming video, VoIP software, or custom script).
Step 2: Start the application to generate UDP traffic.
<img width="1912" height="846" alt="image" src="https://github.com/user-attachments/assets/0593254c-02d8-4ca5-a161-384669754e62" />
Step 3: Start capturing packets in Wireshark while the UDP application is running.
<img width="1919" height="953" alt="image" src="https://github.com/user-attachments/assets/bc1d95a9-bb19-42ba-affd-2aefdc753cf5" />
Step 4: After sufficient traffic is generated, stop capturing packets.
<img width="1919" height="936" alt="image" src="https://github.com/user-attachments/assets/7550ffd3-34d0-4a3b-8d03-69d5c898f19e" />

Task 2: Filter and analysis UDP Packets
Step 1: In the filter bar, type UDP and press Enter.
Step 2: This filters out only the UDP packets from the capture.
<img width="1919" height="935" alt="image" src="https://github.com/user-attachments/assets/e978504c-b5cb-4480-944f-0768a90660c5" />
Step 3: Select any UDP packet to view its details.
<img width="1919" height="688" alt="image" src="https://github.com/user-attachments/assets/d35af6e2-6f76-4f58-aad5-bd1cff9ac593" />
Step 4: Observe the source and destination ports, length, and data.
<img width="1918" height="388" alt="image" src="https://github.com/user-attachments/assets/4d046153-ad71-4e90-a5a4-e2071edb60ee" />
Step 5: Compare the simplicity of UDP headers with TCP headers.
<img width="1612" height="462" alt="image" src="https://github.com/user-attachments/assets/ba4302ad-3110-4229-b148-e9a7e77aed65" />
<img width="1729" height="743" alt="image" src="https://github.com/user-attachments/assets/80f1db9c-9306-412d-ae32-58aebc05b288" />
| Property    | UDP                           | TCP                                     |
| ----------- | ----------------------------- | --------------------------------------- |
| Header Size | 8 bytes                       | 20+ bytes (sometimes more with options) |
| Connection  | Connectionless (no handshake) | Connection-oriented (3-way handshake)   |
| Reliability | Unreliable (no Seq/Ack)       | Reliable (Seq, Ack, retransmission)     |
| Speed       | Faster                        | Slower (because it is reliable)         |


Part 4: Comparing TCP and UDP by filling in the following tables. Save your work (e.g., in an MS Word document), and upload it to your online git repo.

Task 1: Fill in the following table and provide reasons.
|                                          | TCP or UDP  | Reasons                                                                                                                                           |
| -----------------------------------------| ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| Reliability and Connection Establishment | TCP         | TCP is reliable and establishes a connection before sending data (3-way handshake). It ensures all data arrives and retransmits any lost data.
| Data Integrity and Ordering              | TCP         | TCP ensures data arrives in the correct order and does not allow any part to be lost.

Task 2: Identify the use Cases and Performance of TCP and UDP.
|             | TCP                                                                             | UDP                                                                                         |
| ------------| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| Use cases   | Websites, Email, File transfer, Remote access.                                  | Live streaming, VoIP calls, Online gaming, DNS queries.                                     |
| Performance | Reliable and safe, but slower because it checks that all data arrives in order. | Very fast, doesn’t guarantee delivery, can lose some data, good for live or streaming apps. |


