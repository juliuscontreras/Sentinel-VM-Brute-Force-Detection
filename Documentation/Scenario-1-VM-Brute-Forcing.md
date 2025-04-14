# Scenario 1: VM Brute-Forcing Lab

## Pre-Lab Explanation
This lab simulates a brute-force attack against an Azure virtual machine (VM) using multiple IP addresses. It includes creating detection rules in Microsoft Sentinel to detect these attacks and the corresponding incident response actions based on NIST 800-61.

## Part 1: Create Alert Rule (Brute Force Attempt Detection)
1. Open Microsoft Sentinel and navigate to the "Configuration" section.
2. Create a new custom query rule using the `Brute-Force-Detection.kql` file.
![image](https://github.com/user-attachments/assets/55d548cd-d0c0-44b3-996e-1267473ec778)

## Part 2: Trigger Alert to Create Incident
1. Generate multiple failed logon attempts against a test VM to trigger the alert.
2. Verify the alert is firing in Sentinel.
![image](https://github.com/user-attachments/assets/85d4b892-0791-4972-959a-5a9f7d469cbc)


## Part 3: Work Incident (following NIST 800-61)
1. Analyze the incident and confirm the failed logon attempts.
2. Use the `Check-Successful-Logons.kql` query to ensure no successful logons occurred.
3. Follow containment procedures: Isolate affected VMs and initiate a full scan.
![image](https://github.com/user-attachments/assets/78af6ef1-6b2c-4779-b70e-d4bd2a4427e6)


## Part 4: Cleanup
1. Review logs for any lingering suspicious activity.
2. Lock down RDP access using `NSG-Lockdown.kql`.
3. Document the findings and complete the incident response steps.

