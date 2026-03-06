## Creating a Baseline Device Group

A dynamic device group was created in Microsoft Intune to represent all managed Windows endpoints.

Group Name:
Baseline - Corporate Windows Devices

Group Type:
Security

Membership:
Dynamic Device

Dynamic Rule Used:
(device.deviceOSType -contains "Windows")

Purpose:
This group ensures all newly enrolled Windows devices automatically receive required enterprise applications.
