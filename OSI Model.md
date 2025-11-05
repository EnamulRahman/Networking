Open Systems Interconnection (OSI) Model

Definition:
A standard framework that defines how devices and applications communicate across a network.
It has 7 layers, each responsible for specific network functions.

OSI Model Layers (Top to Bottom)

Layer 7 – Application

Closest to the end user.

Provides network services directly to applications.

Examples: HTTP, FTP, SMTP, DNS.

Layer 6 – Presentation

Ensures data is in a usable format for the application layer.

Handles data encryption, compression, and translation (syntax layer).

Layer 5 – Session

Manages sessions between applications.

Handles connection establishment, maintenance, and termination.

Layer 4 – Transport

Provides end-to-end communication and data delivery.

Uses TCP and UDP to manage transmission.

Handles error checking, sequencing, and flow control.

Layer 3 – Network

Responsible for routing and forwarding data packets.

Determines how data is sent from source to destination.

Devices: Routers

Data unit: Packets

Layer 2 – Data Link

Handles node-to-node communication within the same network.

Uses MAC addresses for device identification.

Devices: Switches, Bridges

Data unit: Frames

Layer 1 – Physical

Transmits raw bits (0s and 1s) over a physical medium.

Includes cables, hubs, repeaters, and wireless signals.

TCP/IP Model

Definition:
A simplified, practical model used in real-world networking — built from the OSI model.

Layers:

Application Layer

Combines OSI layers 5–7.

Protocols: HTTP, HTTPS, DNS, TLS, SMTP.

Transport Layer

Manages end-to-end communication.

Protocols: TCP, UDP.

Internet Layer

Responsible for logical addressing and routing.

Protocol: IP (Internet Protocol).

Network Access Layer

Combines OSI layers 1 and 2.

Handles physical transmission and data link control.

Sender & Receiver Perspective (Encapsulation/Decapsulation)

Sender:
Data moves from Layer 7 → Layer 1, gaining headers as it travels down (encapsulation).

Receiver:
Data moves from Layer 1 → Layer 7, headers are removed (decapsulation) to interpret the data.

Ports and Protocols Overview

Ports

Logical endpoints for communication on a device.

Example: Port 80 (HTTP), Port 443 (HTTPS), Port 25 (SMTP).

Protocols

Rules that define how data is formatted and transmitted.

Ensure smooth communication between devices and applications.

TCP vs UDP

TCP (Transmission Control Protocol)

Connection-oriented — requires a handshake before communication.

Reliable and ensures data arrives accurately and in order.

Includes error checking and flow control.

Think of TCP as the postman of the internet — careful and reliable.

Examples: Web browsing, email, file transfer.

UDP (User Datagram Protocol)

Connectionless — no handshake, no guarantee of delivery or order.

Fast but less reliable.

Ideal for real-time or streaming applications (speed > accuracy).

Examples: Video streaming, DNS queries, VPNs.
