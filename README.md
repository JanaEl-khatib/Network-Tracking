# Network-Tracking
This Python script parses captured network traffic from a `.pcap` file (e.g., exported from Wireshark), extracts IP address pairs, geolocates them using the MaxMind GeoLiteCity database, and generates a KML (Keyhole Markup Language) file for visualizing network paths in Google Maps.

## Features

- Parses packets from a PCAP file using `dpkt`
- Extracts source and destination IP addresses
- Uses `pygeoip` and GeoLiteCity database to geolocate IPs
- Generates a KML file with geospatial lines between communicating IPs
- Designed for cybersecurity traffic analysis or geolocation visualization

## File Overview

- `GeoLiteCity.dat` — Legacy IP geolocation database from MaxMind
- `Packets.pcap` — Your Wireshark-exported network traffic file
- `main.py` — The script to run
- Output: Printed KML data to be saved manually or redirected to a `.kml` file

## Requirements

- Python 3.x
- Install required packages:

```bash
pip install dpkt pygeoip
