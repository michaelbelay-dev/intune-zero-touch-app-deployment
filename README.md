# Enterprise Device Baseline Application Deployment (Microsoft Intune)

## Project Overview
This project demonstrates how to configure mandatory baseline applications that automatically install on newly enrolled corporate devices using Microsoft Intune.

Instead of assigning applications to specific users, applications are deployed to devices using device-based assignments. This ensures that all new computers receive required software before the user signs in.

This simulates a real-world enterprise workstation provisioning workflow.

---

## Technologies Used
- Microsoft Intune
- Azure Active Directory
- Microsoft 365
- Win32 App Deployment
- Windows 10/11 Enterprise Devices

---

## Project Scenario
In this scenario, a new workstation was prepared for an employee docking station setup.  
The user was not present to log in, but required applications still needed to be installed.

To solve this, a **device-based deployment model** was implemented so that software installs automatically regardless of user login.

---

## Key Objective
Create a baseline application deployment model where all managed devices automatically install required enterprise applications.

Examples:
- Adobe Creative Cloud
- Google Chrome
- Zoom
- Security / Endpoint tools

---

## Architecture
Admin → Intune Portal → Device Group Assignment → Managed Endpoint → Automatic Application Installation

---

## Deployment Strategy

### Step 1 — Device Enrollment
Verify the device is enrolled and managed by Microsoft Intune.

### Step 2 — Application Packaging
Applications are uploaded as Win32 packages into Intune.

### Step 3 — Baseline Device Group
Create or use a device group such as:

A dynamic device group was created to automatically include all Windows devices enrolled in Intune.

This allows administrators to deploy required applications to all corporate endpoints without targeting individual users.
Corporate Windows Devices

This group represents all managed endpoints.

### Step 4 — Required Application Assignment
Applications are assigned as:

Required  
Install Behavior: System Context  
Target: Device Group

This ensures apps install even before user login.

### Step 5 — Device Sync
The device syncs with Intune policies and downloads the required applications.

### Step 6 — Installation Verification
Deployment status is monitored through:

Intune → Apps → Device Install Status

---

## Skills Demonstrated
- Enterprise endpoint management
- Device-based deployment strategy
- Application packaging and deployment
- Zero-touch workstation provisioning
- Intune administration
- IT automation mindset

---

## Real-World Enterprise Use Case
Large organizations prepare laptops before shipping them to employees.  
When the device connects to the internet and syncs with Intune, required applications automatically install.

This reduces:
- Manual IT setup time
- Support tickets
- Security risks
- Deployment inconsistencies

---

## Future Improvements
- Add additional baseline applications
- Implement Autopilot provisioning
- Create compliance policies
- Deploy security baseline policies
- Automate provisioning workflows
