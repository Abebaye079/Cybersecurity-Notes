- describes seven layers that computer systems use to communicate over a network.
- Each layer of the OSI model interacts with the layer directly above and below it, ==encapsulating and transmitting data== in a structured manner.

#### - Application Layer: HCI layer, where applications can access the network service.
	- provide protocols and services that are used by the applications to communicate
	- Functionality: resource sharing, remote file access, network management
	
#### - Presentation Layer:  translate data between  app layer and network format
	- ensures that data sent from the application layer of one system is readable by the application layer of another system.
	- This layer handles data ==formatting, encryption, and compression==, facilitating interoperability between different systems.
	-  It transforms data into a format that the application layer can understand.

#### Session Layer: manages and controls the connection between computers
	- control ports and sessions
	- It establishes, maintains, and terminates connections

#### Transport Layer: segments and reassembles data for efficient transmission 
	- Transmit data using transmission protocols including TCP and UDP}
	- TCP ( is connection oriented and ensures reliable data transfer with error checking and flow control ) and UDP ( connectionless, fast, less reliable, )

#### Network Layer: is responsible for data routing, forwarding, and addressing.
	- decide which physical path the data will take
	- manages logical addressing through IP addresses and handles packet forwarding.
	- protocols: IP for routing and addressing and ICMP, RIP

#### Data Link Layer: responsible for node-to-node data transfer and error detection and correction.
	- ensures that data is transmitted to the correct device on a local network segment
	- manages MAC address and divide into 2 sublayers

#### Physical Layer: is responsible for the physical connection between devices.
	-  defines the hardware elements involved in the network, including cables, switches, and other physical components


Real example:  sending an email to a person overseas

1. when a user sends it starts at application layer. the email uses SMTP  to handle the email message
2. passed to presentation layer. it is formatted and encrypted 
3. to session layer, session established between the sender's and receiver's server
4. reaches transport layer, divide to smaller packets
5. each packet assigned source and destination IP address in network layer
6. Data Link layer uses MAC address to handle packets' journey across local networks
7. physical layer converts the data into electrical signals, transmitted over fiber optic cables under Atlantic ocean


Upon reaching the recipient’s server in London, the process is reversed:

-  The Physical Layer converts the signals back into data packets, which are reassembled at the Data Link Layer.
- The Network Layer ensures the packets have arrived correctly, and the Transport Layer reorders them if necessary.
- The Session Layer maintains the session until the email is fully received.
- The Presentation Layer decrypts and formats the email, and the Application Layer delivers the email to the client, where it appears in their inbox.