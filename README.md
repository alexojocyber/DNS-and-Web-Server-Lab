# DNS and Web Server Lab

## Overview

This project demonstrates the configuration of a DNS server and a web server in Cisco Packet Tracer. The lab verifies that clients can access a website using a domain name instead of an IP address.

## Objectives

- Configure a router and switch
- Assign static IP addresses to all devices
- Configure a DNS server
- Create DNS records
- Configure a web server
- Test network connectivity
- Verify DNS resolution through a web browser

---

## Network Topology

| Device | IP Address |
|----------|----------|
| Router0 | 192.168.10.1 |
| DNS Server | 192.168.10.2 |
| Web Server | 192.168.10.3 |
| PC0 | 192.168.10.10 |

---

## Topology Diagram

```text
              Router0
                 |
              Switch0
             /   |   \
            /    |    \
     DNS Server Web Server PC0
```

---

## Router Configuration

```bash
enable

configure terminal

interface gigabitEthernet0/0
 ip address 192.168.10.1 255.255.255.0
 no shutdown

end

write memory
```

---

## DNS Configuration

| Record Name | IP Address |
|------------|------------|
| company.local | 192.168.10.3 |

---

## Web Server Configuration

HTML page:

```html
<h1>Welcome to Alex's Enterprise Network Lab</h1>
<p>DNS resolution is working successfully!</p>
```

---

## Verification Commands

### Router

```bash
show ip interface brief
show running-config
```

### PC

```cmd
ping 192.168.10.1
ping 192.168.10.2
ping 192.168.10.3
```

### Browser Test

```text
http://company.local
```

---

## Results

- Router connectivity verified
- DNS server configured successfully
- Web server configured successfully
- DNS resolution working
- Website accessible through `company.local`

---

## Troubleshooting

### Issue 1: Duplicate IP addresses

**Problem:**

Multiple devices shared the same IP address.

**Solution:**

Assigned unique IP addresses to all devices.

---

### Issue 2: Packet Tracer cache problem

**Problem:**

Packet Tracer displayed "IP address already in use."

**Solution:**

Deleted and recreated the affected devices.

---

### Issue 3: Connectivity failure

**Problem:**

PC0 could not ping the router or servers.

**Solution:**

Recreated the PC and DNS server and reassigned IP addresses.

---

## Skills Demonstrated

- DNS configuration
- Web server deployment
- Static IP addressing
- Router configuration
- Network troubleshooting
- Connectivity testing
- Cisco Packet Tracer
