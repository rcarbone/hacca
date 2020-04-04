![logo]

hacca - C implementation of HL7 Standard Protocols
==========================================================

```
-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=
            _                         
           | |__   __ _  ___ ___ __ _ 
           | '_ \ / _` |/ __/ __/ _` |
           | | | | (_| | (_| (_| (_| |
           |_| |_|\__,_|\___\___\__,_|

    hacca - C Toolkit and Applications for HL7 Protocol

    R. Carbone (rocco@tecsiel.it)
    1Q 2020

    SPDX-License-Identifier: BSD-2-Clause-FreeBSD

-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=-=
```

# What is hacca?

**hacca** is a C implementation of HL7 Services and Protocols to connect medical equipments, middlewares and laboratory systems over TCP/IPv4 networks.

**hacca** includes a lot of software modules:

 * **libhacca** - a C library to enable C-written applications to establish, use and release multiple connections with peer applications for the purpose to exchange HL7 Messages/Segments in a network end-system architecture based on the TCP/IP Protocols accordingly to HL7 international standards.

 * **h7sh** - The first HL7 shell for Linux Systems, implemented as a clone of the [tcsh] shell with extensions to add HL7 commands, that include fileutils, connections, HL7 Messages generators and senders over TCP/IPv4 Networks. **h7sh** may be used as both an interactive tool for talking with medical applications and instruments using HL7 Protocols and an interpreter for the execution of testsuites.


 * **hl7c** - a tiny-compiler able to convert raw HL7 text files to C data structures (variables/structures/functions) for direct inclusion in C applications. Used mainly for development and a definition of consistent QA test environment.


 * **libhl7-files** - a tiny C library for working with in memory HL7 files each with its own Messages/Segments. Used mainly for development and a definition of consistent QA test environment.

 * standalone binary programs to play with HL7 Protocols including:
   * fileutils          (hcat, hc, hdump, htree)
   * production servers (hvald, haccad)
   * testing servers    (hnulld, hnakd, hackd, hslowd)
   * testing clients    (hrain, hsndfile)
   * testing generators (hgen)
   * tools              (such a general-purpose hacca-plugins loader to build and run complex architetures)

# Dockerhub
An interactive Docker image based on GNU/Debian bullseye-slim (to be minimalist!) can be found here:

```
    https://hub.docker.com/r/roccocarbone/hacca
```

and can be easily pulled and run with the following commands:
```
   user@somehost 1> docker pull roccocarbone/hacca:latest
   user@somehost 2> docker run -it roccocarbone/hacca:latest
```

It is an interactive container, meaning that the Docker-CLI will talk directly with the HL7 shell included in the image.

## Screenshots

#### A quick tour to h7sh available commands.

  ## Hello World!
  ![helloworld]

  ## Additional HL7 commands
  ![help]

  ## Connecting/Disconnecting to/from a HL7 Server ...
  ![connect]

  ## Establishing multiple connections to a HL7 Server ...
  ![multiple]


[logo]:       images/hacca.png
[helloworld]: images/helloworld.png
[help]:       images/help.png
[connect]:    images/connect.png
[multiple]:   images/multiple.png
