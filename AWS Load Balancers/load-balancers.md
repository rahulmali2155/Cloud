# AWS Load Balancers (ALB, NLB, GWL

In simple words, an **AWS Load Balancer** is like a **traffic police officer** standing in front of your servers.

Instead of all users directly hitting one server, the load balancer **receives traffic and distributes it** to healthy servers so no single server gets overloaded.

AWS mainly has 3 modern load balancers under **Elastic Load Balancing (ELB)**:

---

# 1. Application Load Balancer (ALB)

Think of ALB as a **smart receptionist**.

It understands **HTTP/HTTPS (web traffic)** and can make decisions based on the request content.

## Example

A user visits:

* `example.com/api` → Send to backend servers
* `example.com/images` → Send to image servers
* `shop.example.com` → Send to shopping app

ALB can inspect:

* URL path
* Hostname
* Headers
* Query string

## Use ALB When

✅ Running websites / web apps
✅ Microservices
✅ APIs
✅ Need path-based routing

## Real Example

Suppose you host:

* React frontend
* Java backend
* Node API

One ALB can route all of them.

## Architecture

```text
User → ALB → EC2 / ECS / Kubernetes Pods
```

---

# 2. Network Load Balancer (NLB)

Think of NLB as a **super-fast highway toll gate**.

It does **very little thinking**, but handles traffic **extremely fast**.

It works at **Layer 4 (TCP/UDP)**.

It only looks at:

* IP
* Port
* Protocol

It does **NOT care about URLs or paths**.

## Use NLB When

✅ Need ultra-low latency
✅ Millions of requests/sec
✅ TCP / UDP applications
✅ Gaming, VoIP, databases

## Examples

* MySQL database cluster
* Game server
* SSH service

## Architecture

```text
Client → NLB → Servers
```

## Special Feature

NLB can provide **static IP addresses**, which is useful for firewall whitelisting.

---

# 3. Gateway Load Balancer (GWLB)

This one confuses many people initially.

Think of GWLB as a **security checkpoint**.

It is not mainly for normal web traffic balancing.

It is used to **insert security appliances** into network traffic.

## Security Appliances Examples

* Firewall
* IDS / IPS
* Packet inspection
* Deep traffic analysis

## Traffic Flow

```text
User Traffic → GWLB → Firewall Appliance → Application
```

## Use GWLB When

✅ Centralized security inspection
✅ Third-party firewall appliances
✅ Need packet inspection

## Example

A company wants every packet inspected before entering the VPC.

GWLB sends traffic to security appliances automatically.

---

# Easy Memory Trick

* **ALB = Application** → Web / HTTP
* **NLB = Network** → Fast TCP / UDP
* **GWLB = Gateway** → Security / Firewall
