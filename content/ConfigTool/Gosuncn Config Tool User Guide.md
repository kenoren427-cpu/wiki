# Gosuncn ConfigTool User Guide

## Introduction

This guide provides instructions for using the **ConfigTool** to configure your device — including server IP/port, APN, and other parameters. Please contact a Gosuncn engineer for assistance when configuring the device.

**Supported Models:** GD201 / GD302 / GD303 / GD506 / GD105 / GL103 / GT115 / GT117 / GT118 / GT161

> [!NOTE]
> - GD105 only supports firmware upgrades.
> - The tool only displays features supported by the selected model.

## Table of Contents

[toc]

---

## Setup Device

### Setup Device for Tracker (GT115 as Example)

1. Connect the device to the debug board using a custom 10-pin debug cable.
2. Connect the debug board to the PC via USB Type-C.
3. Power the device with 12V / 24V.

> [!NOTE]
> The debug board and 10-pin connector are custom accessories. Please contact us if needed.

![[Attachments/Pasted image 20260427124850.png|318]]

### Setup Device for OBD (GD303 as Example)

1. Connect the device to the debug board.
2. Connect the debug board to the PC via Micro USB.
3. Power the device with 12V / 24V.

![[Attachments/Pasted image 20260427124736.png|327]]

---

## Setup ConfigTool

1. Obtain the ConfigTool from a Gosuncn engineer or development kit.

   ![[Attachments/Pasted image 20260427130436.png|76]]

2. Double-click **ConfigTool-1.X.X-Win64.msi** and follow the installation wizard.

   ![[Attachments/Pasted image 20260427130541.png|334]]

### Install UART Serial Driver (Optional)

- Run **CP210xVCPInstaller_x64.exe** or **CP210xVCPInstaller_x86.exe** (depending on your system) to install the driver.
- The serial driver is located in the **Driver** folder under the ConfigTool root directory.

> [!NOTE]
> The UART serial driver is automatically installed when you install the ConfigTool. If the automatic installation fails, install it manually.

---

## Verify Driver Installation

1. Open **Device Manager** and check for the USB-to-UART device. If installed correctly, it should appear as shown below.
2. Different devices may display different device names; as long as the driver functions normally, it is ready to use.

![[Attachments/Pasted image 20260427130618.png|382]]

---

## Launch ConfigTool

1. Launch the ConfigTool, as shown below.

   ![[Attachments/Pasted image 20260427130648.png]]

2. Select the device model by clicking the product name.
3. Click **Open port** to connect to the device.
4. When the icon turns blue, the connection is successful.

---

## User Guide

The user guide is integrated into the ConfigTool. Click the **Help** button to view it.

![[Attachments/Pasted image 20260427130823.png|394]]

The path of the user guide:

![[Attachments/Pasted image 20260427130845.png|429]]

---

## Configuration

You can set parameters such as **APN**, **Server**, **GNSS**, etc., via the ConfigTool. For details, refer to the user guide.

- Click the **Settings** icon to open the configuration window.

![[Attachments/Pasted image 20260427130903.png|360]]

---

## Capture System Log

You can use the ConfigTool to capture system logs. Follow the steps below:

> [!NOTE]
> Administrator privileges are required to access and capture system logs. Contact a Gosuncn engineer to obtain the username and password.

1. Click **View** in the ConfigTool window.
2. Click **Admin** to open the login window.
3. Enter the **Username** and **Password** (default: `admin` / `admin`).
4. Click **Login**.

   ![[Attachments/Pasted image 20260427153244.png|425]]

5. A new **Log** button will appear.

   ![[Attachments/Pasted image 20260427153313.png|415]]

6. Click the **Log** button to open the log window. For detailed operations, refer to the user guide.

---

## Upgrade Firmware

1. Use the ConfigTool to upgrade the system and Bluetooth firmware, as shown below.

   ![[Attachments/Pasted image 20260427154053.png]]

> [!NOTE]
> Administrator privileges are required to upgrade the bootloader.

2. Click **Firmware** in the ConfigTool window to enter the firmware upgrade window. Select the firmware file and click **Done**.

   ![[Attachments/Pasted image 20260427154004.png|414]]

3. Wait for the update to complete (approximately 3 minutes).

   ![[Attachments/Pasted image 20260427154304.png|418]]

## Troubleshooting

### The Serial Port Driver Is Not Loaded Normally

**Question:**  
The USB-to-UART device icon shows a yellow exclamation mark, indicating the PC cannot recognize the serial port.

![[Attachments/Pasted image 20260427154403.png|362]]

**Solution:**  
Reinstall the correct USB-to-UART driver. Contact the board vendor or Gosuncn technical support for assistance.

### Connect Device Failed

**Question:**  
When setting the correct parameters, the following message appears:  
*"Please check the device connection and try again."*

![[Attachments/Pasted image 20260427154439.png]]

**Solution:**

1. Check the device LED indicators. If no LED is illuminated, the device may be powered off or in sleep mode. Check the power supply, or gently shake the device to wake it.
2. Check if the cable is securely connected.
