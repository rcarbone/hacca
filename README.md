# What is hacca?

**hacca** is a C implementation of HL7 2.x Services and Protocols to connect medical equipments, middlewares and laboratory systems over TCP/IPv4 networks.

![logo]

hacca - C implementation of HL7 2.x Standard Protocols
==========================================================

```
-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=
            _                         
           | |__   __ _  ___ ___ __ _ 
           | '_ \ / _` |/ __/ __/ _` |
           | | | | (_| | (_| (_| (_| |
           |_| |_|\__,_|\___\___\__,_|

    hacca - C Toolkit and Applications for HL7 2.x Protocol

    R. Carbone (rocco@tecsiel.it)
    1Q 2020

    SPDX-License-Identifier: BSD-2-Clause-FreeBSD

-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=
```

# Docker container for the impatients

If you are impatient and not interested in the full story, here is the download button for a docker image with **hacca** in an interactive container based on GNU/Debian bullseye-slim (to be minimalist!):
```
    https://hub.docker.com/r/roccocarbone/hacca
```

The container is interactive, meaning that the Docker-CLI will talk directly with the **h7sh** (HL7 shell) included in the image.
It can be easily pulled and run using the following commands:

* docker pull roccocarbone/hacca
* docker run -it roccocarbone/hacca

![impatiens]

# About

**hacca** includes a lot of software modules:

 * **libhacca** - a C library to enable C-written applications to establish, use and release multiple connections with peer applications for the purpose of exchanging HL7 2.x Messages/Segments in a network end-system architecture based on the TCP/IP Protocols accordingly to HL7 international standards.

 * **h7sh** - The first HL7 2.x shell for Linux Systems, implemented as a clone of the **tcsh** shell with extensions to add HL7 2.x commands, that include fileutils, connections, HL7 2.x Messages generators and senders over TCP/IPv4 Networks. **h7sh** may be used as both an interactive tool for talking with medical applications and instruments using HL7 2.x Protocols and an interpreter for the execution of testsuites.

 * **hl7c** - a tiny-compiler able to convert raw HL7 text files to C data structures (variables/structures/functions) for direct inclusion in C applications. Used mainly for development and a definition of consistent QA test environment.

 * **libhl7-files** - a tiny C library for working with in memory HL7 files each with its own Messages/Segments. Used mainly for development and a definition of consistent QA test environment.

 * standalone binary programs to play with HL7 2.x Protocols including:
   * coreutils          (hsegs, hdescribe, hnamespace)
   * fileutils          (hcat, hc, hdump, htree)
   * testing servers    (hnulld, hnakd, hackd, hslowd)
   * testing clients    (hrain, hsndfile)
   * testing generators (hgen)
   * production servers (hvald, haccad)
   * tools              (such a general-purpose hacca-plugin loader to build and run complex architetures)

## Screenshots

#### A quick tour to h7sh available commands.

  ## Hello World!
  ![helloworld]

  ## Additional HL7 2.x commands
  ![help]

  ## Connecting/Disconnecting to/from a HL7 2.x Server ...
  ![connect]

  ## Establishing multiple connections to a HL7 2.xServer ...
  ![multiple]

[logo]:       images/hacca.png
[impatiens]:  images/impatiens.png
[helloworld]: images/helloworld.png
[help]:       images/help.png
[connect]:    images/connect.png
[multiple]:   images/multiple.png
