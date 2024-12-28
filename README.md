# One-Line Quines

This is a collection of one-line quines in several languages. A quine is a program that outputs its own source code, and in theory such a program exists for any Turing-complete programming language with an output feature (essentially all programming languages in common use today).

Although the quines are only one line, they are not attempts to find the shortest quines possible. Many "redundant" parts are kept to maintain some readability and good style. The quines are also meant to be portable across a wide variety of implementations, although some alternatives are provided that make certain assumptions.

All code is dedicated to the public domain under [Creative Commons CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) (a copy is available in `LICENSE.txt`).

Note: Some files have a newline at the end while others do not. This is intentional because the output functions available in different languages either add a newline or omit it. In most cases it is easy to adjust the program to either add or remove a newline at the end of the file.

## Assembly

Programs are available for Linux on x86 (32-bit), Linux on x86-64, and DOS on x86 (16-bit), and are written for the GNU Assembler. They do not depend on the C standard library and should be statically linked. By their very nature, these programs are not portable across platforms.

The DOS program requires a separate linker script to set the output format and memory addresses.

GNU Assembler requires a newline at the end of the source code, although it only gives a warning and still assembles the code without it. The code can be shortened if the newline is omitted.

## AWK

The program is compatible with POSIX.1-2004. The input is not used.

## C

The main program is compatible with C89 and makes very few assumptions. The code can be shortened a bit by assuming that the character encoding is ASCII (`olq_ascii.c`) and also by assuming support for POSIX-style positional format specifiers (`olq_posix.c`). (Of course, these two assumptions may be combined.)

The declaration for `printf` at the beginning is needed because other code cannot be on the same line as an `#include`, which poses a problem for a one-line program.

## C#

The main program is compatible with C# 1.0 and essentially all implementations of the BCL. The code can be shortened substantially by using top-level statements, introduced in C# 9 (`olq_cs9.cs`).

## Clojure

The program is compatible with Clojure 1.0.

## Emojicode

The program is compatible with Emojicode 0.7.0 and later (latest version tested is Emojicode 1.0 beta 2).

## F#

The program is compatible with F# 2.0.

## Forth

The program is compatible with ANS Forth.

## Go

The program is compatible with Go 1.

## Haskell

The program is compatible with Haskell 98.

## Java

The program is compatible with Java SE 5 (when the `PrintStream.printf` and related string formatting methods were added).

## JavaScript

The main program is compatible with ECMAScript 5 (when the JSON functions were added). The code can be shortened by using some ECMAScript 6 features (`olq_es6.js`), namely template literals and arrow functions.

## Lua

The program is compatible with Lua 5.0.

## Perl

The main program is compatible with Perl 5.8.0 (when the POSIX-style positional format specifiers were introduced for `printf`). Like in C, the main program does not assume a particular character encoding, although it does use POSIX-style positional format specifiers as mentioned previously. The code can be shortened a bit by assuming that the character encoding is ASCII (`olq_ascii.pl`).

## PHP

The program is compatible with PHP 4.

## Python

The main program uses the `str.format` method introduced in Python 3, even though the code that uses the older printf-style string formatting (`olq_percent.py`) is shorter.

## Ruby

The program is compatible with Ruby 2.0.

## Rust

The program is compatible with Rust 1.0.

A previous version of the program is adapted from a [submission to Programming-Idioms.org](https://www.programming-idioms.org/idiom/182/quine-program/4063/rust), originally added by r0t0m0l0t0v. That code is available under [Creative Commons Attribution-ShareAlike 3.0 Unported](https://creativecommons.org/licenses/by-sa/3.0/) (a copy is available in `LICENSE-Rust.txt`), as it is derived from code that uses that license.

## Scheme

The program is compatible with R5RS.

## Shell

The program is compatible with the POSIX shell language as defined in POSIX.1-2004.