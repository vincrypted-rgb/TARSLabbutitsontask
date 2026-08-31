# JPCERT Tool Analysis Result Sheet

In this lab, we will be taking an in depth look at a digital forensics tool designed to help **identify lateral movement** and *other malicious activity* within a system or network.
It covers **49** different **Windows-Native tools** "which are likely to be used by the attacker that has infiltrated a network."

> [!TIP]
> This document reflects observed behaviors from 49 tools tested in a controlled environment. It is not a comprehensive signature database, nor is it intended to be treated as a definitive answer key. Malicious actors use a wide range of tools: some Windows-native, some Linux-based, some *entirely other*. The conditions that existed during this testing will almost never align perfectly with those of a live incident.
>
> Treat the Result Sheet as a *reference point, not an answer key*. If the activity you're investigating appears here, use it as a guiding point. If it doesn't, use the logic behind this sheet to give direction for your next steps. 

You do **not** need a VM. However, the first link is the Result sheet itself and highly recommended for this lab. The second is the mentioned "report" in the result sheet. It's a good read and *may* help with understanding the usage and methodology behind the result sheet.

> [!IMPORTANT]
> [JPCERT Tool Analysis Result Sheet](https://jpcertcc.github.io/ToolAnalysisResultSheet/)
> 
> [Detecting Lateral Movement through Tracking Event Logs (Version 2)](DetectingLateralMovementThroughTrackingEventLogs_version2)

Upon accessing the result sheet, I'd familiarize myself with its' purpose and contents. Any unfamiliar vocabulary, and especially this table:

[table_1](table_1)

Pop quiz! (When you're ready. Multiple answers are possible, but is not always guaranteed or required. Pick what you think is the most correct. LOOK UP THE ANSWERS YOU NEED TO KNOW THESE TERMS)

#1. **What is an event log?** *(0/2)*
- [ ] The Windows specific app designed to allow users to monitor event creation, execution, and other processes
- [x] The written record of a singular action run by a computer.
- [x] A time-ordered digital diary that records actions, errors, and messages happening inside a computer system or software
- [ ] a hard disk drive. they call it that because the data gets logged to the HDD permanently. Kinda like wood carving. Haha, get it. event log. shoulda called it a data log. ah well, missed opportunities.

#2. What is execution history?
- [ ] I don't know man I'm not king henry viii
- [x] Recorded data or logs that show when applications, commands, or background tasks were previously run.
- [ ] A list of every single time you have logged off your computer
- [ ] The Artificial Intelligence's plan to take over. You weren't supposed to see that.

#3. What's Prefetch? What's the file extension for it?
- [ ] malware; .ps1
- [ ] accessibility file; .reg
- [ ] auto-update; .msi
- [x] memory performance tool; .pf

#4. What does the "USN" in USN Journal stand for?
- [x] Update Sequence Number
- [ ] Unrealistically Slow Network
- [ ] Universal Serial Number
- [ ] Unexpected Screaming Newsletter

#5. What does the MFT have in it?
- [ ] IP Addresses
- [ ] Personal files and emails
- [x] Metadata
- [ ] Python

#6. What does UserAssist track?
- [ ] Command line usage
- [x] Launching apps out of a GUI (graphical user interface)
- [ ] Use of, and happiness with the accessibility features. And request to clean up printers.
- [ ] How little your mouse moves. It's designed to keep you focused in the workplace.

#7. What is a Packet? Why do malicious actors want to capture them? 
- [x] Unit of data being sent over the internet; gives access to session and network info in a way that might make someone vulnerable
- [ ] Evil hacker mwuahahahah ; it was the only thing they could figure out.
- [ ] A hardware component used to encrypt security keys; to siphon your PCIe speeds and hack you while your computer is slow
- [ ] a food?; because they're hungry?

#8. What two things would someone looking to use the Result Sheet need to set up before their system would start logging the correct events? *(0/2)*
-  [ ] Windows subsystem for Linux
-  [x] Audit Policy
-  [x] Sysmon (and a configuration file)
-  [ ] Wireshark
