# 🧑‍💻 IT Home Lab Portfolio - Sarian Szumowski

## 🎯 Introduction and Project Goals
The main goal of this portfolio is to document practical knowledge in IT Support, specifically by building a virtual home environment (Home Lab) which includes an on-premise Active Directory setup and a Hybrid Cloud connection.

---

## 🚀 Project 1: Virtualization Host Setup (VirtualBox)

### 1.1. Goal and Hypervisor Selection
* **Goal:** To create a stable and isolated testing environment for Project 2 (Active Directory).
* **Selected System:** Oracle VirtualBox (Chosen due to compatibility with the Windows Home edition host OS).

### 1.2. Host Requirements Verification
* **Host OS Version:** Windows 11 Home. (Confirmed that Hyper-V is not available, necessitating the use of VirtualBox).

![Host OS Version - Windows 11 Home](https://github.com/user-attachments/assets/bd0e753e-fb20-4c7e-9bc3-9e46c7898123)

<img width="579" height="588" alt="image" src="https://github.com/user-attachments/assets/790fe4d8-6146-4492-ba81-ee32f066ef7a" />

### 1.3. Host CPU Virtualization Check (BIOS/UEFI Fix)

**The Challenge:** Initial inspection via Task Manager confirmed that the required CPU virtualization feature (Intel VT-x / AMD-V) was **disabled** in the host machine's BIOS/UEFI settings, blocking full hypervisor functionality.

#### 1. Initial State: Virtualization **Disabled**

**Evidence (Before Fix):**
Showing the Task Manager view with Virtualization explicitly reported as 'Disabled'.
![Task Manager - Virtualization Disabled](https://github.com/user-attachments/assets/bd0e753e-fb20-4c7e-9bc3-9e46c7898123)

---

#### 2. Verification: Virtualization **Enabled**

**Action Taken:** The BIOS/UEFI settings were accessed, and the 'Intel Virtualization Technology' (or equivalent) feature was successfully set to 'Enabled'.

**Evidence (After Fix):**
Showing the Task Manager view after reboot, confirming the successful change. This confirms the host system is now ready for Project 2.
![Task Manager - Virtualization Enabled](https://github.com/user-attachments/assets/866b7cbb-ca63-45a8-91b7-382b0631d7a6)

<img width="587" height="630" alt="image" src="https://github.com/user-attachments/assets/866b7cbb-ca63-45a8-91b7-382b0631d7a6" />

