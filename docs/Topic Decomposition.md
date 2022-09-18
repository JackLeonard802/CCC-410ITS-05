# IoT Extraction and Analysis Topic Decomposition

![image](https://user-images.githubusercontent.com/71239122/190930443-eb7938e3-ff88-4580-8731-50681da6b810.png)


# Outline

# IoT Extraction/Analysis

## Devices

### Amazon Echo Dot

* Configured/Used

	An Echo with over 2 years of semi-active use, may be a gold mine of data
* Unconfigured

	Serves as a control to compare the used Echo to

### Smart LED strips

These may not send or receive much data, but nonetheless they are internet-connected devices, so they are worth investigating.

### Smart TVs

* Samsung

	Most advanced of the TVs, linked to many accounts and devices
* TCL (with roku)

	Uses the Roku GUI, linked to many personal accounts
* Visio

### Ring Cameras

These cameras are motion-activated, and video footage is stored for at least two months, which indicates an web service used for storage that the cameras upload to. The cameras can detect video, sound, and IR light.

### Xfinity XiOne TV box

This is a completely unconfigured TV box that seems to function similarly to a Roku device. It would serve as a good point of comparison for the Roku enabled TV.

## Tools

### Data Extraction

* Stored Data
	* Binwalk

		This is a firmware extraction tool that can be used to retrieve data from the firmware, and in this case it can be used to retrieve the filesystem of IoT devices
* Data In Transit
	* Network Scan (nmap)

		This would mostly be used to find ports where data might be coming from, allowing for easier filtering in Wireshark. Also allows for OS detection and script scans for more info about how to approach data extraction.
	* Proxy Server

		Easily allows the capture of data in transit if devices use proxy to communicate with the rest of the network. Could be a VM on my laptop, but I might opt for a VM on my ESXi host.
		* Wireshark

			Easily allows for packet data to be captured and analyzed.

### Analysis

* Wireshark Filters

	Allows for saved captures to be narrowed down when looking for specific data. Saves time, and limits number of different products used
* Spreadsheets

	Useful for keeping track of types of data collected, as well as specific items of interest.
