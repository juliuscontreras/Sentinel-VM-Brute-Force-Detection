# NIST 800-61 Incident Response Lifecycle

## Preparation
- Ensure that all VMs are onboarded to Microsoft Defender for Endpoint.
- Create and test alert rules in Microsoft Sentinel.

## Detection and Analysis
- Identify brute-force login attempts via Sentinel alerts.
- Analyze suspicious IPs using KQL queries like `Brute-Force-Detection.kql`.

## Containment, Eradication, and Recovery
- Isolate compromised VMs in MDE.
- Run antimalware scans.
- Restrict RDP access via Network Security Group (NSG).

## Post-Incident Activity
- Conduct a full investigation.
- Document findings and improvements.
- Implement better security policies for future prevention.

## Closure
- Verify that all security issues are resolved.
- Close the incident in Sentinel and document the lessons learned.
