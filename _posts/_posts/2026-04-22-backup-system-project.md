---
layout: post
title: "Project Breakdown: C# Client-Server Backup System"
categories: [Projects, Backend Engineering]
tags: [c-sharp, .net, socket-programming, networking]
---

Building a reliable file synchronization system requires diving deep into low-level networking. Instead of relying on high-level web APIs, I engineered a custom client-server backup application entirely from scratch using **C# and the .NET Framework**.

### Architecture Overview
The system is cleanly decoupled into two main components:
1. **BackupServer:** A resilient backend service that binds to specific network ports, listens for incoming TCP socket connections, and manages the continuous byte streams of incoming file data. It ensures files are written safely to the target storage.
2. **BackupClient:** A dedicated desktop frontend that allows users to configure their backup paths, select files, and initiate the socket connection to the server.

### Technical Highlights
* **Socket Programming:** Managed custom TCP socket connections for raw data transfer, handling packet fragmentation and stream reconstruction.
* **Separation of Concerns:** Maintained strict boundaries between the UI logic and the network transmission layers.
* **Test-Driven Reliability:** Developed a comprehensive `BackupSystemTests` suite to validate file I/O edge cases and network resilience, ensuring data integrity during transfer.
* **Documentation:** Integrated Doxygen to auto-generate extensive API and class hierarchy documentation.

This project served as a deep dive into backend architecture, stream handling, and robust object-oriented design principles.
