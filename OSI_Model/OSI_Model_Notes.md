# <u> -------------------- OSI MODEL -------------------- <u/>


## <u> What Is the OSI Model? <u/>

  - The Open Systems Interconnection (OSI) model describes seven layers that computer systems use to communicate over a network. The OSI model is divided into seven distinct layers, each with specific responsibilities, ranging from physical hardware connections to high-level application interactions.

  - Each layer of the OSI model interacts with the layer directly above and below it, encapsulating and transmitting data in a structured manner. This approach helps network professionals troubleshoot issues, as problems can be isolated to a specific layer. The OSI model serves as a universal language for networking, providing a common ground for different systems to communicate effectively.

  - The OSI model was the first standard model for network communications, adopted by all major computer and telecommunication companies in the early 1980s. It was introduced in 1983 by representatives of the major computer and telecom companies, and was adopted by ISO as an international standard in 1984.

  - The modern Internet is not based on OSI, but on the simpler TCP/IP model. However, the OSI 7-layer model is still widely used, as it helps visualize and communicate how networks operate.


## <u> Why Is the OSI Model Important? <u/>

The OSI model provides several advantages for organizations managing networks and communications:

  - Shared understanding of complex systems : OSI offers a universal language for networking, enabling different network devices and software to communicate. By dividing communication into seven distinct layers, it allows network professionals to isolate and troubleshoot problems effectively.
    
  - Faster research and development : Developers can focus on improving specific layers without affecting others, leading to more rapid innovations. This modular approach enables specialization and enables different teams to work on various aspects of network communication simultaneously.
    
  - Flexible standardization : The model’s layered approach allows for the integration of new technologies at any layer without disrupting the overall network structure. This ensures compatibility across different devices and protocols, ensuring long-term viability and scalability of network infrastructure.


## <u> OSI Model Explained : The OSI 7 Layers <u/>

We’ll describe OSI layers “top down” from the application layer that directly serves the end user, down to the physical layer.

### 7. Application Layer
   
The Application Layer serves as the interface between the end-user applications and the underlying network services. This layer provides protocols and services that are directly utilized by end-user applications to communicate across the network. Key functionalities of the Application Layer include resource sharing, remote file access, and network management.

  - Examples of protocols operating at the Application Layer include Hypertext Transfer Protocol (HTTP) for web browsing, File Transfer Protocol (FTP) for file transfers, Simple Mail Transfer Protocol (SMTP) for email services, and Domain Name System (DNS) for resolving domain names to IP addresses. These protocols ensure that user applications can effectively communicate with each other and with servers over a network.

### 6. Presentation Layer

The Presentation Layer, also known as the syntax layer, is responsible for translating data between the application layer and the network format. It ensures that data sent from the application layer of one system is readable by the application layer of another system. This layer handles data formatting, encryption, and compression, facilitating interoperability between different systems.

  - One of the key roles of the Presentation Layer is data translation and code conversion. It transforms data into a format that the application layer can understand. For example, it may convert data from ASCII to EBCDIC. It also includes encryption protocols to ensure data security during transmission and compression protocols to reduce the amount of data for efficient transmission.

### 5. Session Layer

The Session Layer manages and controls the connections between computers. It establishes, maintains, and terminates connections, ensuring that data exchanges occur efficiently and in an organized manner. The layer is responsible for session checkpointing and recovery, which allows sessions to resume after interruptions.

  - Protocols operating at the Session Layer include Remote Procedure Call (RPC), which enables a program to execute a procedure on a remote host as if it were local, and the session establishment phase in protocols like NetBIOS and SQL. These services enable reliable communication, especially in complex network environments.

### 4. Transport Layer

The Transport Layer provides end-to-end communication services for applications. It ensures complete data transfer, error recovery, and flow control between hosts. This layer segments and reassembles data for efficient transmission and provides reliability with error detection and correction mechanisms.

  - Protocols at this layer include Transmission Control Protocol (TCP) and User Datagram Protocol (UDP). TCP is connection-oriented and ensures reliable data transfer with error checking and flow control, making it suitable for applications like web browsing and email. UDP is connectionless, offering faster, though less reliable, transmission, suitable for applications like video streaming and online gaming.

### 3. Network Layer

The Network Layer is responsible for data routing, forwarding, and addressing. It determines the best physical path for data to reach its destination based on network conditions, the priority of service, and other factors. This layer manages logical addressing through IP addresses and handles packet forwarding.

  - Key protocols at this layer include the Internet Protocol (IP), which is important for routing and addressing, Internet Control Message Protocol (ICMP) for diagnostic and error-reporting purposes, and routing protocols like Routing Information Protocol (RIP) that manage the routing of data across networks.

### 2. Data Link Layer

The Data Link Layer is responsible for node-to-node data transfer and error detection and correction. It ensures that data is transmitted to the correct device on a local network segment. This layer manages MAC (Media Access Control) addresses and is divided into two sublayers: Logical Link Control (LLC) and Media Access Control (MAC).

  - Protocols and technologies at this layer include Ethernet, which defines the rules for data transmission over local area networks (LANs), and Point-to-Point Protocol (PPP) for direct connections between two network nodes. It also includes mechanisms for detecting and possibly correcting errors that may occur in the Physical Layer.

### 1. Physical Layer

The Physical Layer is responsible for the physical connection between devices. It defines the hardware elements involved in the network, including cables, switches, and other physical components. This layer also specifies the electrical, optical, and radio characteristics of the network.

  - Functions of the Physical Layer include the modulation, bit synchronization, and transmission of raw binary data over the physical medium. Technologies such as Fiber Optics and Wi-Fi operate at this layer, ensuring that the data physically moves from one device to another in the network.


## <u> Advantages of OSI Model <u/>

The OSI model helps users and operators of computer networks :

  - Determine the required hardware and software to build their network.
  - Understand and communicate the process followed by components communicating across a network.
  - Perform troubleshooting, by identifying which network layer is causing an issue and focusing efforts on that layer.

The OSI model helps network device manufacturers and networking software vendors :

  - Create devices and software that can communicate with products from any other vendor, allowing open interoperability
  - Define which parts of the network their products should work with.
  - Communicate to users at which network layers their product operates – for example, only at the application layer, or across the stack.

### How Does Communication Happen in the OSI Model? A Practical Example in image format included with some other information in another file (OSI_Model_Images.md).
