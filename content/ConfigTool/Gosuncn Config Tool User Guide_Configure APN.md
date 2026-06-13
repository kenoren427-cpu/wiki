# Gosuncn ConfigTool User Guide — Configure APN

---

## Introduction

This guide provides instructions for using the ConfigTool to configure your device — including server IP/port, APN, and other parameters. Contact a Gosuncn engineer for assistance if needed.

**Supported Models:** GD201 / GD302 / GD303 / GD506 / GD105 / GL103 / GT115 / GT117 / GT118 / GT161

> [!NOTE]
> - GD105 supports firmware upgrades only.
> - The tool displays features supported by the selected model.

---

## Setup ConfigTool
  
![../../01_项目管理/Configtool/Attachments/Pasted image 20260427130436.png](app://02bd85a289c1017995d4f77e03211c2f49bd/D:/08project/Obsidian/Obsidian/01_%E9%A1%B9%E7%9B%AE%E7%AE%A1%E7%90%86/Configtool/Attachments/Pasted%20image%2020260427130436.png?1777266276216)
**Step 1:** Obtain the ConfigTool from a Gosuncn engineer or from the link below.
![[../../01_项目管理/Configtool/Attachments/Pasted image 20260427130436.png]]**Download Link:** [Google Drive — ConfigTool Package](https://drive.google.com/drive/folders/1GUSEKKuG0ofV-j1fM38CiDhUsZlyuEiI?usp=sharing)
**Step 2:** Double-click **ConfigTool-1.X.X-Win64.msi** to launch the installer and follow the on-screen instructions.

![[Attachments/Pasted image 20260427130541.png|334]]

---

### Install UART Serial Driver (Optional)

- Run **CP210xVCPInstaller_x64.exe** or **CP210xVCPInstaller_x86.exe** (depending on your system) to install the driver.
- The serial driver is located in the **Driver** folder under the ConfigTool installation root directory.

> [!NOTE]
> The UART serial driver is installed automatically during ConfigTool installation. If the automatic installation fails, install it manually.

---

## Verify Driver Installation

**Step 1:** Open **Device Manager** and check for the USB-to-UART device. If the driver is installed correctly, the device should appear as shown below.

**Step 2:** Different devices may display different device names; as long as the driver functions normally, it is ready to use.

![[Attachments/Pasted image 20260427130618.png|382]]

---

## Launch ConfigTool

**Step 1:** Launch the ConfigTool, as shown below.

![[Attachments/Pasted image 20260427130648.png]]

**Step 2:** Select the device model by clicking the product name.

**Step 3:** Click **Open port** to connect the device.

**Step 4:** The connection is successful when the icon turns blue.

---

## User Guide

A user guide is integrated into the ConfigTool. Click the **Help** button to view it.

![[Attachments/Pasted image 20260427130823.png|394]]

The path of the user guide:

![[Attachments/Pasted image 20260427130845.png|394]]

---

## Configuration

You can configure parameters such as **APN**, **Server**, **GNSS**, etc., using the ConfigTool. For details, refer to the user guide.

- Click the **Settings** icon to open the configuration window.

![[Attachments/Pasted image 20260427130903.png|360]]

---

## Configure APN

**Step 1:** Navigate to **Network**, enter the APN in the **Name** field, then click **Apply**.

![[Attachments/Pasted image 20260427130903.png|360]]

**Step 2:** Navigate to **General** and click **Restart Device** to reboot the device. The APN configuration will take effect.

---

## Capture System Log

You can use the ConfigTool to capture system logs. Follow the steps below:

> [!NOTE]
> Administrator privileges are required to access and capture system logs. Contact a Gosuncn engineer to obtain the username and password.

**Step 1:** Click **View** in the ConfigTool window.

**Step 2:** Click **Admin** to open the login window.

**Step 3:** Enter the **Username** and **Password** (default: `admin` / `admin`).

**Step 4:** Click **Login**.

![[Attachments/Pasted image 20260427153244.png|425]]

**Step 5:** A new **Log** button will appear.

![[Attachments/Pasted image 20260427153313.png|415]]

**Step 6:** Click the **Log** button to open the log window. For detailed operations, refer to the user guide.

---

## Upgrade Firmware

**Step 1:** Use the ConfigTool to upgrade the system and Bluetooth firmware, as shown below.

![[Attachments/Pasted image 20260427154053.png]]

> [!NOTE]
> Administrator privileges are required to upgrade the bootloader.

**Step 2:** Click **Firmware** in the ConfigTool window to enter the firmware upgrade window. Select the firmware file and click **Done**.

![[Attachments/Pasted image 20260427154004.png|414]]

**Step 3:** Wait for the update to complete (approximately 3 minutes).

![[Attachments/Pasted image 20260427154304.png|418]]

---

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
