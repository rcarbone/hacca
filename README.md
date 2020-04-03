# What is hacca?

hacca is a C implementation of HL7 Services and Protocols to connect medical equipments, middlewares and laboratory systems over TCP/IPv4 networks.

hacca supports creation, parsing and transmission of HL7 Messages over TCP/Iv4 networks accordingly to HL7 international standards.

[hacca] includes a lot of software modules:

 * libhacca - a C library for creating/packing/unpacking HL7 Segments/Messages and transmitting them over IPv4 Networks.

   It is implemented as a library of ANSI C language functions enabling C-written applications to establish, use and release multiple connections
   with peer applications for the purpose to exchange HL7 Messages in a network end-system architecture based on the TCP/IP Protocols.


 * h7sh - The first HL7 shell for Linux Systems

   It is implemented as a clone of the [tcsh] shell with extensions to add HL7 commands, that include fileutils, connections, HL7 Messages generators and senders over TCP/IPv4 Networks.

   [h7sh] may be used as both an interactive tool for talking with medical applications and instruments using HL7 Protocols and an interpreter for the execution of testsuites.


 * hl7c - a tiny-compiler able to convert raw HL7 text files to C data structures (variables/structures/functions) for direct inclusion in C applications.
   Used mainly for development and consistent QA test environment.


 * libhl7-files - a tiny C library for working with in memory HL7 files each with its own Messages/Segments.
   Used mainly for development and consistent QA test environment.


 * standalone binary programs to play with HL7 Protocol including:
   - fileutils          (hcat, hc, hdump, htree)
   - production servers (hvald, haccad)
   - testing servers    (hnulld, hnakd, hackd, hslowd)
   - testing clients    (hrain, hsndfile)
   - testing generators (hgen)
   - tools              (such a general-purpose hacca-plugins loader to build and run complex architetures)

# Dockerhub
A simple Debian Linux container can be found here:
> https://hub.docker.com/r/roccocarbone/hacca

and can be easily pulled with the following command:
> docker pull roccocarbone/hacca

It is an interactive container, meaning that the Docker-CLI will talk directly with the [h7sh] shell included in the container.
