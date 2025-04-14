# Scenario 1: VM Brute-Forcing Lab

## Pre-Lab Explanation
This lab simulates a brute-force attack against an Azure virtual machine (VM) using multiple IP addresses. It includes creating detection rules in Microsoft Sentinel to detect these attacks and the corresponding incident response actions based on NIST 800-61.

## Part 1: Create Alert Rule (Brute Force Attempt Detection)
1. Open Microsoft Sentinel and navigate to the "Configuration" section.
2. Create a new custom query rule using the `Brute-Force-Detection.kql` file.

## Part 2: Trigger Alert to Create Incident
1. Generate multiple failed logon attempts against a test VM to trigger the alert.
2. Verify the alert is firing in Sentinel.

## Part 3: Work Incident (following NIST 800-61)
1. Analyze the incident and confirm the failed logon attempts.
2. Use the `Check-Successful-Logons.kql` query to ensure no successful logons occurred.
3. Follow containment procedures: Isolate affected VMs and initiate a full scan.

## Part 4: Cleanup
1. Review logs for any lingering suspicious activity.
2. Lock down RDP access using `NSG-Lockdown.kql`.
3. Document the findings and complete the incident response steps.
