# SMAnitoring
A repository containing different ways to monitor an SMA solar inverter (SMA Wechselrichter or SMA Omvormer) equipped with WLAN or Ethernet.

# Overview

Each SMA inverter equipped with Speedwire (the proprietary name for the SMA technology to monitor an SMA inverter over TCP) can be monitored in different ways. One of them is https://github.com/SBFspot/SBFspot but due to privacy concerns or more granular measurement data one could opt to monitor the SMA inverter locally.

# Local Administration Web Page (LAP)

A (recent) SMA inverter which has been connected to your network via either WLAN or Ethernet will serve a local administration portal (LAP) when you browse to the IP of the inverter.

You can logon to the inverter with a user-account (default password: 0000) or an installer-account (default password: 1111). This in turn will give you a valid session (and Session ID) and present you with a detailed view of your inverter and statistics.

The interesting pane when monitoring your SMA is the "Instantaneous Values" tab. The LAP requests a JSON containing all values displayed there. We will be using this JSON to do our own monitoring and magic. 

When one would open the Developer Tools in Chrome they could see that the webpage requests the JSON by doing a POST to the IP/hostname of the SMA with a payload and with a SID.

The equivalent cURL command for this request and getting the JSON is described in:

//insert ref to file curl command


# JSON

The JSON can be parsed with JSONPath or similar tools to extract all values.

// insert ref to file with JSON paths
