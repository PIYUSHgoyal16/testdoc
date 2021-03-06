---
title: IPP scan (or virtual MF device) server (Scanner Application)
---
The Printer Working Group (PWG) has also taken multi-function devices into account, devices which offer printer and scanner in one unit. For that they have added IPP Scan, an extension of the existing IPP protocol to facilitate driverless scanning. As IPP is already in use by the operating systems for many years via CUPS, using it as a scanning standard in the operating system makes it easy to integrate network multi-function devices.

Currently, to scan in linux, a user has to procure the device specific SANE driver and then use a command line or a GUI based application that communicates with that scanner using this driver. Using IPP-Scan, a client would be able to communicate and receive files from an IPP-Scan enabled scanner using a universal IPP-Scan SANE backend or more directly via an IPP implementation, like for example libcups, thus eliminating the need of maintaining scanner specific drivers. 

However, currently there are no IPP-Scan scanners on the market. Scanner Applications attempt to remedy this situation by connecting to ordinary scanners and then emulating the IPP-Scan scanner for them. The clients can now communicate with the Scanner Application as if they were communicating with an IPP-Scan scanner. This provides us with two major benefits, firstly we move all the drivers to the central scan service rather than keeping a copy of each driver on each client and secondly, developers can now distribute sandboxed packages of the scanner drivers.

Feel free to discuss in the comments.
