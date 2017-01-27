[![Build Status](https://api.travis-ci.org/opensatelliteproject/libsathelper.svg?branch=master)](https://travis-ci.org/opensatelliteproject/libsathelper) [![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](https://tldrlegal.com/license/mit-license)


libSatHelper
==================

Helper library for decoding Satellite Signals.

Features
=========

*   Viterbi27 Decode / Encode (wrapper from [libcorrect](https://github.com/quiet/libcorrect))
*   CCSDS ReedSolomon Decode (wrapper from [libcorrect](https://github.com/quiet/libcorrect))
*   ReedSolomon [De]Interleaver
*   Correlator for Sync Word
*   Packet Phase Ambiguity Fixer (For 0, 90, 180, 270 degrees and IQ Inversion)
* Working on Windows

How to build
============

This Library depends on [libcorrect](https://github.com/quiet/libcorrect). Please make sure you have it installed before trying to compile SatHelper.

The **libsathelper** can be compiled in three modes: `Debug Shared`, `Release Shared`, `Release Static`. The `static` and `shared` refers to the linking mode of the library (the shared will generate a **.so** file and static will generate a **.a** file). For example GOES LRIT Decoder have Shared and Static builds using **libsathelper**.

For compiling, just enter on one of the folders `Debug`, `Release`, `Release (Static)` and run `make`. You can also use `Eclipse CDT` to compile the project.

How to build (Windows)
======================

TODO: Now we use [libcorrect](https://github.com/quiet/libcorrect) instead libfec.

OLD:

```
For windows it should be compiled using Microsoft Visual C++ compiler (it should work with mingw, but not tested). First you need to compile the modified [libfec](https://github.com/racerxdl/libfec) that can compile in mingw32 and generate the msvc libraries (everything described on libfec's readme). After that create a folder named `winfec` and copy the `fec.h`, `libfec.lib`, `libfec.exp`. Then you shoud be able to compile `libSatHelper.dll` in Visual Studio. The Solution was made in Visual Studio 2015
```
