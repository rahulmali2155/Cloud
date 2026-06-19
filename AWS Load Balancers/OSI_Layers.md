# OSI Model (Open Systems Interconnection)

The **OSI Model** is a framework that explains **how data travels from one computer to another over a network**.

Think of it like **sending a parcel** from your home to a friend.

Before the parcel reaches your friend:

* You pack the item
* Write the address
* Give it to delivery service
* It travels through roads
* Finally gets delivered

Similarly, when data travels over a network, it passes through **7 layers**.

Each layer has a specific job.

---

# Why Do We Need OSI?

The OSI model helps us:

* Understand how network communication works
* Troubleshoot network problems
* Identify where an issue is happening

Example:

* Website not opening?
* Ping working but SSH not working?
* DNS issue?

OSI helps determine which layer has the problem.

---

# The 7 Layers of OSI

Data travels from **Layer 7 → Layer 1** when sending
Data travels from **Layer 1 → Layer 7** when receiving

---

# Layer 7 — Application Layer

This is the layer closest to the user.

It is where **applications interact with the network**.

Examples:

* Web browser
* Email client
* WhatsApp
* API requests

Protocols:

* HTTP
* HTTPS
* FTP
* DNS
* SMTP

## Simple Example

You open Chrome and visit a website.

That request starts at the Application Layer.

---

# Layer 6 — Presentation Layer

This layer handles **data formatting, encryption, and compression**.

Its job is to make sure both systems understand the data format.

Examples:

* Encryption (SSL/TLS)
* JPEG
* MP4
* JSON/XML formatting

## Simple Example

When you visit an HTTPS website, encryption happens here.

---

# Layer 5 — Session Layer

This layer manages **connections (sessions)** between devices.

It controls:

* Starting session
* Maintaining session
* Ending session

## Simple Example

You join a Zoom meeting.

Session layer keeps the connection active until you leave.

---

# Layer 4 — Transport Layer

This layer ensures data reaches correctly.

It handles:

* Reliability
* Error checking
* Segmentation
* Flow control
* Port numbers

Protocols:

* TCP
* UDP

## Simple Example

TCP ensures all packets arrive correctly.

UDP is faster but doesn’t guarantee delivery.

Examples:

* Video streaming → UDP
* Banking website → TCP

---

# Layer 3 — Network Layer

This layer decides **where data should go**.

It handles:

* IP addressing
* Routing
* Path selection

Protocol:

* IP

Device:

* Router

## Simple Example

Like Google Maps choosing the best route to destination.

---

# Layer 2 — Data Link Layer

This layer handles communication between devices on the same network.

It uses:

* MAC address
* Frames
* Switches

Device:

* Switch

## Simple Example

Your Wi-Fi router sending data to your laptop inside home network.

---

# Layer 1 — Physical Layer

This is the actual physical connection.

Examples:

* Ethernet cable
* Fiber cable
* Wi-Fi signals
* Electrical signals

It sends raw bits:

* 0
* 1

## Simple Example

The actual wires carrying internet data.

---

# Easy Real-Life Analogy

Sending a WhatsApp photo:

| Layer          | Example                     |
| -------------- | --------------------------- |
| 7 Application  | WhatsApp app                |
| 6 Presentation | Compress / encrypt photo    |
| 5 Session      | Keep chat connection active |
| 4 Transport    | Break data into packets     |
| 3 Network      | Choose route using IP       |
| 2 Data Link    | Send inside local network   |
| 1 Physical     | Wi-Fi / Cable               |

---

# Easy Memory Trick

Remember this:

**All People Seem To Need Data Processing**

* A → Application
* P → Presentation
* S → Session
* T → Transport
* N → Network
* D → Data Link
* P → Physical

---
