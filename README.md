# Building-R-4-for-Windows-with-OpenBLAS

The details of the codeset and plots are included in the attached Microsoft Word Document (.docx) file in this repository. 
You need to view the file in "Read Mode" to see the contents properly after downloading the same.

A Brief Introduction
====================

This post outlines the steps needed to build R 4+ for Windows with OpenBLAS. The release of R 4.0 includes significant changes to the Windows build system from prior versions—for the better! Before anything, we all owe Jeroen Ooms significant gratitude for the many hours he spent working on the build system. Thank you, Jeroen!!

The build process below creates an installation file for both 32-bit and 64-bit R but makes some compromises. Extra time spent building the installer is traded for reduced time spent adjusting files and minimizing needed file changes. The OpenBLAS library itself is built using the “dynamic” keyword so it will work for all architectures, and it is built to use up to 64 threads. It isn’t completely optimized to the actual building CPU, which is not only reasonable but necessary. A centralized library must be generic enough to serve all comers. Eventually, I hope to refine the process to build just the 64 bit version and to link to a static, locally-compiled, and locally-optimized OpenBLAS library.  For now, installation as binaries should work.
