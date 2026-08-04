# Troubleshooting

## Problem 1

PC0 could not obtain an IP address.

### Cause

Duplicate IP addresses were assigned to the DNS server and web server.

### Solution

Assigned unique IP addresses to all devices.

---

## Problem 2

Packet Tracer displayed "IP address already in use".

### Cause

Packet Tracer cached the previous configuration.

### Solution

Deleted and recreated the affected devices.

---

## Problem 3

PC0 could not ping the router.

### Cause

The PC network interface configuration became corrupted.

### Solution

Recreated the PC and DNS server and reconfigured them.

---

## Verification

- Successful ping tests
- DNS resolution successful
- Website accessible through `http://company.local`