---
layout: post
title: GO toolchain  
tags: [go,GO]

---

## The GO tool-chain
The GO tool-chain(which is used to compile apps) supports application development.  Itprovides for testing, formatting, and documentation, as well as package management.

## Project Structure
When you develop GO applications the toolchain expects that you use a "workspace" that has a specific folder and directory structure.  This in a sense is similar to ROR rails, which has a folder structure also.

## Terminology 
* Packages
  * Packages are contained in a single directory
  * All .go files must declare the package they belong to in the first line of the file.
  * You cannot have multiple packages in a directory, NOR can packages cross directories.  Meaning all .go files in a directory declare the same package.
  * The convention is that the package name be the same as the directory.
* Package main - "main" has a special meaning in Go, telling the Go command that the package will be compiled into a binary executable.  A "main" package is **required** for all executable packages.
  * Each package main must have a function main() which is the entry point for the program.   The binary will take the name of the directory where main package is declared in.
  




