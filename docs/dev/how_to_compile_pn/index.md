---
layout: up
title: How to Compile PN
---
## Requirements:

  * [Microsoft Visual Studio 2013 Community](http://www.visualstudio.com/en-us/news/vs2013-community-vs.aspx) (free)
  * [Git](http://git-scm.com/downloads/guis)
  * [Subversion](http://subversion.tigris.org/)
  * [Boost](http://www.boost.org/) library: 1.57

## Pre-requisite Installation

  - Download the boost library (link above)
  - Extract boost somewhere on your HD.  You don't need to build it, since PN
  will only use the headers (unless you're building boost-python or test libs,
  in which case see the [building boost libs](http://www.pnotepad.org/docs/dev/building_Boost_libs)
  page).
  - Get WTL (head from subversion: `svn co https://wtl.svn.sourceforge.net/svnroot/wtl/trunk/wtl wtl`)
  - Edit the file `properties/pn.props` in Visual Studio and fix the paths to WTL and Boost that you've just installed.

## Fetch and Build Steps

  - Get the PN code from Github: `git clone https://github.com/simonsteele/pn.git`
    - Note: Depending on your source control client's setup you may then need to add execute permissions to DLL and EXE files in the bin directory.  You'll know that you do if, when you come to run pn.exe (see below), you get a c0000022 exception.
  - Now go to pnwtl/ and open the "pn.sln" file with Visual Studio.
  - Build the solution and then run pn.exe.
