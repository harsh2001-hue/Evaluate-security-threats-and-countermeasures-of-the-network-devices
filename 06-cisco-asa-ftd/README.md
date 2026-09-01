# CVE-2024-20481 – Cisco ASA/FTD Vulnerability

## 1. Device / Protocol Affected
Impacts Cisco Adaptive Security Appliance (ASA) and Firepower Threat Defense (FTD) devices — extensively used enterprise firewalls for network perimeter protection, traffic filtration, and intrusion prevention.

## 2. Nature of Vulnerability & Severity
- **Severity:** High (CVSS ~7.5–8.5)
- **Attack Type:** Denial of Service (DoS)

Allows an unauthenticated attacker to disrupt network services by sending specifically crafted traffic to the target device.

## 3. Affected Component
- Network packet processing mechanisms
- Traffic inspection apparatus
- Handling of malformed packets

## 4. Root Cause
Inadequate handling of malformed or unexpected network input, resulting in resource depletion or system instability. The system does not sufficiently validate packet structures, and malformed packets trigger abnormal processing behavior, leading to excessive resource use or system failure.

## 5. Exploitation Method
1. Send specifically crafted network packets to the target device
2. Trigger abnormal packet processing behavior
3. Cause resource depletion or system failure
4. Disrupt firewall operations and network services

Remotely exploitable without authentication; attackers may automate this for large-scale DoS campaigns.

## 6. Real-World Attacks
Used to disrupt corporate network services, cause firewall downtime, block legitimate user access, and degrade overall network performance — often as part of coordinated DoS operations against critical infrastructure.

## 7. Impact
**Technical:** Service disruption, device malfunction or forced restart, network unavailability, reduction in security posture

**Business:** Disruption of essential services, financial loss from downtime, reduced productivity, possible SLA violations

This vulnerability primarily impacts the **Availability** component of the CIA triad.

## 8. Mitigation Strategies
**Immediate:** Apply Cisco security patches and firmware updates; reboot affected systems if required

**Network Controls:** Implement traffic filtering and rate limiting; block malformed or suspicious traffic patterns

**Monitoring:** Monitor network traffic for anomalies; deploy IPS; review logs for unusual traffic spikes

**Long-term:** Establish network redundancy and failover protocols; ensure consistent firmware updates; conduct regular security evaluations

## Reference
National Vulnerability Database (NVD) — [CVE-2024-20481](https://nvd.nist.gov/vuln/detail/CVE-2024-20481)

---
*Part of IE3032 Network Security Group Assignment (Group 16) — analysis by Udayanga K.A.H (IT23667228)*
