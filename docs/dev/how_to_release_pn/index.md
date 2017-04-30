---
layout: up
title: How to Release PN
---
## Requirements:

  * [Working PN Build](http://www.pnotepad.org/docs/dev/how_to_compile_pn/)
  * [Git](http://git-scm.com/downloads/guis)
  * [Inno Setup](http://www.jrsoftware.org/isdl.php)
  * [NAnt](http://nant.sourceforge.net/)
  * [POEdit](http://poedit.net/download)
  * [vcvarsallxp.bat](https://github.com/simonsteele/pn/blob/master/pnwtl/tools/vs2013/vcvarsallxp.bat)
  * [depends.exe](http://www.dependencywalker.com/)

## Release Steps

  - Install the above required software, including placing vcvarsallxp.bat in
      C:\Program Files (x86)\Microsoft Visual Studio 12.0\VC
  - Edit deploy.bat to fix the path to nant.exe.
  - Run deploy.bat with the desired version, e.g.: `deploy 2.4.1`
  - If everything works ok, installer will be built into the dist directory
  - Generate a hash of the installer to post on the download page:
    `$(CertUtil -hashfile .\pn2421440_multilang.exe SHA256)[1] -replace " ",""`
