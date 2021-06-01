This is installer for Turbo C++ v4.5 (1995 Year)

Borland Turbo C++ 4.5 (32-bit compiler) (05/07/1997)


**For Windows**

**Installation:**
If the Install program hung after you read the INSTALL.TXT, reboot the system. Install again but this time choose to "SKIP" the INSTALL.TXT. 
Remember to install Adobe Acrobat Reader in order to view the ONLINE-BOOKS.

**Notes:**
This is the FULL CD taken from Borland Turbo C++ 4.5 For Windows. It includes the ONLINE BOOKS as well as the EXAMPLES contained in the original CD.

Also This is installer for Borland C++ 5.02

and also

ID Automation Code 39 (Barcode Generator Installer)


```
/****************************************************************/
                            INSTALL.TXT
                          Borland C++ 5.02
     ---------------------------------------------------------

To jump to a specific section, search for "SECTION #", replacing
the # with the appropriate section number.

--------
CONTENTS
--------

SECTION 0 System Requirements
A. Minimum System Requirements
B. Minimum Installation
C. Full Installation
D. Other Installations 
E. Installation Procedure

SECTION 1. Installation Notes
A. Hard Drive Installation
B. Microsoft PLUS! (tm) Issues
C. CD Installation
D. Files Changed During Installation
E. Files Added at First Startup
F. Removing Registration Reminder
G. Files Available on the CD
H. Installation of Help Files

SECTION 2. Changing Your System Configuration
A. "Clean Boot" under Windows 95
B. "Clean Boot" under Windows NT

SECTION 3. Troubleshooting Installation Error Messages
A. Startup Error Messages
B. Decompression Error Messages

SECTION 4. Registry Changes
A. Key Names and Values
B. File Extension Associations 

SECTION 5. Other Ways to Get Help
A. How to Get Good Phone Support
B. Relevant Telephone Numbers
C. Online Services

-----------------------------
SECTION 0 System Requirements
-----------------------------

A. Minimum System Requirements
------------------------------
To install and run Borland C++ 5.02, you must meet the 
following minimum system requirements:

* 16 MB RAM (24 recommended)
* 80486 processor or better
* Windows 95, Windows NT 3.51 or 4.0
* 25 to 230 MB of free hard disk space (250 MB for the 
  Developer's Suite and 260 MB for the Design Tools), 
  subject to the options you choose (installation options follow)

B. Minimum Installation
-----------------------
A minimum installation of Borland C++ 5.02 includes 
only the command line tools (no IDE), and provides the 
ability to work within another editor and use the command 
line compiler. This setup requires approximately 25 MB of 
hard disk space with 16-bit DOS support.

C. Full Installation
--------------------
A full installation of Borland C++ 5.02 includes all 
the tools available, the Windows-hosted IDE, and allows 
development for 16-bit DOS, 16-bit Windows, and 32-bit Windows. 
This is called the "Typical" install by the installation program, 
and requires 230 MB of hard disk space.

Note: The exact amount of disk space required for installation may 
       vary due to disk cluster size on your PC.

D. Other Installations
----------------------
The following information is provided to allow estimation.

Installation by parts:

	16-bit DOS: 
		 Command line tools:    10 MB
		 Visual tools:          40 MB
		 Libraries:             23 MB
		 Examples:               5 MB
		 Help:                   8 MB

	16-bit Windows:
		 Command line tools:    10 MB
		 Visual tools:          41 MB
		 Libraries:             64 MB
		 Examples:              65 MB
		 Help:                  40 MB

	32-bit Windows:
		 Command line tools:    12 MB
		 Visual tools:          41 MB
		 BDE:                    7 MB
		 Libraries:             90 MB
		 Examples:              69 MB
		 Help:                  47 MB

E. Installation Procedure
-------------------------
IMPORTANT!
Do not install Borland C++ 5.02 over previously installed Borland C++
directories. The files in this distribution will not work with
previously shipped tools and libraries. This is particularly true
for configuration files from previous shipping releases, like 
TDCONFIG.TDW and BCCONFIG.BCW.

We recommend that you do not install Borland C++ to a path that
contains spaces or long filenames because some 16-bit components do
not support long filenames.

To avoid potential conflicts when Setup installs system files, we
recommend that you close down all other running applications before
installing Borland C++.

To update from Version 4.5 or earlier, you need to delete the old
version of Borland C++ from your system before installing Version 5.02.
You also need to delete all references to outdated Help files from your
WINHELP.INI file in your WINDOWS directory. Also, if you have
WinRun in your startup group, unload it before installing
Borland C++ Version 5.02.

To update from Version 5.0, copy the latest uninstall program,
BC5RMV.EXE, from the CD located in the \WINNT or \WIN95 directory to
your current WINDOWS directory.  Then uninstall Borland C++ 5.0 before
installing Borland C++ 5.02.

To install Borland C++ 5.02 from the CD, run \SETUP\BC5\SETUP.EXE.

-----------------------------
SECTION 1. Installation Notes
-----------------------------

A. Hard Drive Installation
--------------------------
Installing from a CD-ROM may cause synchronization 
difficulties between various pieces of hardware or certain 
hardware drivers. If you suspect that your CD-ROM drive or your
CD-ROM driver might be at fault, you can attempt a hard drive
installation.

To begin, copy the entire setup directory into a 
temporary directory on your C:\ drive. The setup directory 
contains all the files needed for the installation. 
Once these have been successfully copied, remove the CD-ROM 
driver from your system configuration by clean-booting, and 
attempt to install the product.

When running the install, remember to change the SOURCE 
directory so that it points to the temporary directory.

B. Microsoft PLUS! (tm) Issues
-------------------------
Under Windows 95 with the PLUS! Pack (tm) installed, 
some floating-point errors may occur. This has been 
traced to a problem in SAGE.DLL, a part of System Agent. 
If this problem occurs, turn OFF System Agent and 
download Plusupd1.exe from:

* Microsoft Network (under mssupport),
* CompuServe (GO MSL), or
* Microsoft's anonymous FTP server 
  (ftp.microsoft.com, Softlib/Mslfiles directory).

Run Plusupd1.exe and follow the instructions on the screen.

C. CD Installation
-----------------
If you choose the CD installation option or the Custom CD 
Installation option, you will not be able to install any 
of the additional products available (such as CodeGuard, 
PVCS, InstallShield, or the Java addon). This is because a 
CD installation leaves the majority of the product in 
write-protected files on the CD-ROM, rather than on the 
hard drive. These write-protected files need to be modified 
to install any of the additional software.

D. Files Changed During Installation
------------------------------------
The following files are changed during installation:

1. WIN.INI  (under Windows 95)  REMIND.EXE is added to the 
   LOAD line of the WIN.INI file:
 
   load=C:\BC5\PIPELINE\REMIND.EXE  
   (where C:\BC5 is where you installed BC5)
  
   OR
   
   Registry key (under Windows NT):
   \\HKEY_CURRENT_USER\SOFTWARE\MICROSOFT\WINDOWS NT
    \CurrentVersion\Windows 

2. SYSTEM.INI  A change is made to the [386Enh] section:
   [386Enh]
   device=C:\BC5\BIN\TDDEBUG.386
   (where C:\BC5 is where you installed BC5)

3. WINHELP.INI  Lists all of the Help files that were installed.

4. OWL.INI is installed.

5. The following files are created if they are not on the system or 
   modify them if they already exist:

   TD.INI
   WORKSHOP.INI
   BCW5.INI
   TDW.INI

E. Files Added at First Startup of the Borland C++ IDE
------------------------------------------------------
Borland C++ creates SPX, SPP, and various configuration 
files in the SCRIPT and BIN directories upon first startup:

default.spp
bcwdef.*
*.SPX, *.CFG, *.BCW, *.DSW, *.MBT, *.MRT

SPX files are compiled versions of cScript files.  
SPP files are uncompiled cScript source files.
The other run-time files store project and desktop settings 
and other configuration information.  Deleting these files 
does no harm to your system and may help with 
troubleshooting IDE configuration problems.


F. Removing Registration Reminder
---------------------------------
If you run the online registration module during Setup and then 
cancel without completing registration, the module adds an EXE to 
your system startup files.  After 14 days, the EXE reminds you to 
register.

Windows 95 users can remove the reminder by editing WIN.INI to delete 
REMIND.EXE from the load= line.

Windows NT users should edit both WIN.INI and the system registry. 
Launch REGEDT32.EXE.  Choose the HKEY_CURRENT_USER window.  Browse to 
this key: Software\Microsoft\Windows NT\CurrentVersion\Windows.  Edit
the value named "load." 


G. Files Available on the CD
----------------------------
Many files are available on your BC5 CD which are not installed 
on your machine's hard drive to save space. Here is a list of 
the kinds of files that you can find:

Example EXE files, 
and support files            In \bc5\examples subdirectories

CodeGuard versions
of libraries                 In \bc5\lib\cg

Debug versions
of libraries                 In \bc5\lib
(OWLD*, BIDSD*, OCFD*)

Runtime library source       In \bc5\source\rtl

RTL startup code             In \bc5\lib\startup

MFC library source           In \bc5\source\mfc

H. Installation of Help Files
-----------------------------
If you do install Borland C++ 5.02 over an existing 
5.0 installation, you must delete all of the hidden 
.GID files in the BC5\HELP directory before using 
the online Help system again. Otherwise, you will see 
a gray dialog with an OK and Cancel button and no error 
message when you try to use Help.

If you uninstall Borland C++ 5.0, then install 5.02 to 
a different directory, you must manually delete all 
entries in the WINHELP.INI file in the WINDOWS 
directory that refer to the old BC5\HELP directory. 
Otherwise, the effect is the same as above.

---------------------------------------------
SECTION 2. Changing Your System Configuration
---------------------------------------------
Although Windows 95 and Windows NT are much more stable 
than Windows 3.1, it is still recommended that you change
the configuration of your system if you encounter problems
when installing new software.  Each operating system has 
its own method, as follows.

A. "Clean Boot" under Windows 95
--------------------------------
Under Windows 95, the method of obtaining a "clean boot"
is through the use of Safe Mode, a boot option provided by 
Microsoft to aid Windows 95 users.

1. Shut down the machine and reboot it.
2. Before the Windows 95 splash screen appears, press and hold 
   down F8.
3. Select Safe Mode from the menu and press Enter.
   You are now running under Windows 95 Safe Mode. 
   Windows 95 will inform you that you are running in a 
   special diagnostic mode with a window.  Click 'OK'
   and you will be able to continue your work.

Note:  Windows 95 will not recognize most CD-ROM drives
       in Safe Mode.  If this is the case for your machine, 
       you'll need to copy the files from the SETUP 
       directory and the Setup.exe on the CD onto your hard
       drive and install from there.


B. "Clean Boot" under Windows NT
--------------------------------
To perform a "clean boot" on an NT machine:
1. Shut down the machine and reboot it.
2. When the OS choice menu appears, select number 2, 
   Windows NT Workstation <version #> [VGA mode].
   Windows NT will then boot itself in a clean mode.


------------------------------------------------------
SECTION 3. Troubleshooting Installation Error Messages
------------------------------------------------------

A. Startup Error Messages
-------------------------
1. "Unable to open install configuration file."

   Problem: SETUP.CFG is not present in the same
   directory as SETUP.EXE. 

   Solution: Move SETUP.CFG to the directory that SETUP.EXE
   is in.

2. "Corrupt install configuration file. Click OK to 
   exit."

   Problem: SETUP.CFG does not have the correct format.

   Solution: The configuration file for the setup 
   is corrupt. Contact the disk replacement phone 
   number listed at the end of this document to obtain 
   a new disk.

3. "Unable to load string resource (#)."

   Problem: A string resource needed by the installation 
   program cannot be found.

   Solution: If this error occurs, contact the installation
   support line number listed at the end of this document.

4. "Cannot execute SETUP.EXE (or one of its components). 
   Check to ensure that all required components 
   (INSTXTRA.PAK) are available."

   Problem: The installation program cannot execute all or
   part of the SETUP. 

   Solution: Make sure INSTXTRA.PAK is located in the same 
   subdirectory as SETUP.EXE.

5. "Cannot execute SETUP.EXE (or one of its components). 
   Check to ensure that all required components (SETUP.CFG) 
   are available."

   Problem: The installation program cannot execute all 
   or part of the SETUP.

   Solution: Make sure SETUP.CFG is located in the same 
   subdirectory as SETUP.EXE and is getting copied to the 
   TEMP directory correctly.

6. "Internal Error: -69. Unable to start installation."

   Problem: Unable to start main installation component.
   This occurs when Windows fails to launch instrun.exe. 
   This could be because:
   * The system is out of memory or resources.
   * The specified file (instrun.exe, in this case)
     was not found.
   * The specified path (usually %TEMP%) was not
     found.
   * The .exe file is invalid (non-Win32 .exe or 
     an error in the .exe image).

   Solution: Ensure that all of the above conditions have 
   been met.

7. "Unable to locate USER.DLL." or
   "Unable to locate comctl32.dll"

    Problem:  You are trying to install Borland C++ 5.02 
    under a 16-bit version of Windows (Windows 3.x).

    Solution: Do NOT install this product under a 16 bit 
    version of Windows.  This product will not install or run
    under 16 bit Windows.  You MUST install this product under
    a 32-bit version of Windows, such as Windows 95 or
    Windows NT 4.0.

B. Decompression Error Messages
-------------------------------
1. "Error during unpacking <name of .pak file>."

   Problem (possibilities):
   * The .pak file referenced in the error 
     message contains one or more files that already
     exist on the system. These files are most 
     likely write protected, or the directory they 
     reside in is write protected, or the files
     are in use by a currently running program.
   * The .pak file is corrupted on the CD or 
     diskette.
   * The installation engine is having difficulty 
     with the synchronization of the CD drive and 
     the rest of the machine. 

   Solutions:
   * Remove the write protection and then try 
     continuing with the installation.
   * Check the CD or diskette for any bad sectors,
     and call the disk replacement phone number listed 
     at the end of this document if necessary.
   * Attempt a hard drive installation as specified 
     in SECTION 1. Installation Notes.
   * Close applications running in the background.
   * Move the file(s) contained in that .pak file 
     out of the directory they are currently resident
     in and into another, temporary directory.

2. "Archive file <name of file> contains a file that 
   cannot be unpacked."

   Problem: The installation engine cannot unpack one of 
   the files contained within the .pak file referenced in 
   the error message.

   Solutions: 
   * Check the disk for bad sectors and call the disk 
     replacement phone number listed at the end of this
     document.
   * Call the installation support number listed at the 
     end of this document for information about 
     attempting a manual installation of Borland C++ 5.02.

3. "Archive file <name of file> is corrupted and 
   cannot be unpacked."

   Problem: The .pak file is either corrupted on the CD 
   or it is getting corrupted in the copying process.

   Solutions: 
   * Check the CD to ensure that the .pak file there 
     is not corrupted. If the CD has a bad sector or 
     track, call the disk replacement phone number 
     provided at the end of this document.
   * If the CD is not damaged, attempt a hard drive 
     installation or attempt to slow the machine 
     down if it is encountering speed synchronization 
     problems with the hardware.

4. "Unable to write to destination file (disk full?) 
   <name of file>."

   Problem: The hard disk already contains a 
   write-protected copy of the file.

   Solution: Remove the write protection and 
   continue with the install.

5. "386 or better required to expand archive 
   <name of file>."

   Problem: Your microprocessor is running too fast.

   Solution: Try slowing down your system by taking 
   your machine out of turbo mode and disabling any
   software that speeds your machine up, such as 
   SmartDrive. If necessary, you can also disable 
   BIOS caching and shadow RAM.


---------------------------
SECTION 4. Registry Changes
---------------------------

The registry under Windows 95 and Windows NT is the 
file where information concerning all software added to the
system is logged and kept for reference. You can access the 
registry by using the registry editor (regedit or regedt32 
under Windows NT) to view and change the registry if necessary.
(There is almost never a reason to do this manually.) The 
following is a list of changes made to the registry when 
Borland C++ 5.02 is installed.

A. Key Names and Values
-----------------------
Key Name: SOFTWARE\Borland\Borland C++\5.0
Class Name: <no class>

Value 0
	Name:	BCRoot Path
	Data:	c:\BC5

Value 1
	Name:	BGI Path
	Data:	c:\BC5\BGI

Value 2
	Name:	Class Library Source Path
	Data: 	c:\BC5\SOURCE\CLASSLIB

Value 3
	Name:	Examples Path
	Data:	c:\BC5\EXAMPLES

Value 4
	Name:	Include Path
	Data:	c:\BC5\INCLUDE

Value 5
	Name:	Lib Path
	Data:	c:\BC5\LIB

Value 6
	Name:	Local BCRoot Path
	Data:	c:\BC5\BIN

Value 7
	Name:	Local Configuration Path
	Data:	c:\BC5\BIN

Value 8
	Name:	Local Help Path
	Data:	c:\BC5\HELP

Value 9
	Name:	OCF Source Path
	Data:	c:\BC5\SOURCE\OCF

Value 10
	Name:	OWL Source Path
	Data:	c:\BC5\SOURCE\OWL

Value 11
	Name:	VDBT Source Path
	Data:	c:\BC5\SOURCE\VDBT

This assumes that you installed to your c:\ drive. If you 
installed to a different drive, then change the drive letter 
accordingly.

Values 6 and 8 are only created when a CD Only installation
or a Network installation (by an End User as opposed to an
Administrator) is performed.

B. File Extension Associations
------------------------------
These are the file extension associations kept in the 
registry under HKEY_CLASSES_ROOT:

HKEY_CLASSES_ROOT\.c   = "cfile"
		 \.cpp = "cppfile"
		 \.h   = "CHeaderFile"
		 \.hpp = "CHeaderFile"
		 \.ide = "idefile"
		 \.rc  = "rcfile"
		 \.res = "resfile"
		 \.spp = "sppfile"

HKEY_USERS
\.Default\.Default\Software\Borland\Borland C++\5.0

HKEY_CURRENT_USER
Software\Borland\Borland C++\5.0
Software\Microsoft\Windows\Help
.Default\Software\Borland\Borland C++\5.0

HKEY_LOCAL_MACHINE
Software\Borland\Borland C++\5.0
Software\Borland\Database Engine
Software\Borland\BLW32
	
Under Windows NT 4.0
Software\Microsoft\Windows\CurrentVersion\App Paths\BCW.EXE

Under Windows NT 3.51
Software\Microsoft\Windows NT\CurrentVersion\App Paths\BCW.EXE

Under Windows 95
Software\Microsoft\Windows\CurrentVersion\App Paths\BCW.EXE
	 

---------------------------------
SECTION 5. Other Ways to Get Help
---------------------------------

A. How to Get Good Phone Support
--------------------------------
* Be prepared to go through the Borland phone tree.
* Have your name, PIN #, product, and version number 
  ready. This will speed the pace of your call.
* Be sure to have read all the relevant documentation.
  Often you can avoid a long-distance or toll 
  call by searching through the documentation.
* Be prepared to describe in detail exactly what you
  have done so far while working on the problem.
* If you've already talked to an engineer, be able 
  to describe what you did while working with that engineer.
* Please be patient. We try to answer all customer 
  questions as thoroughly as possible.

B. Relevant Telephone Numbers
-----------------------------
Main Switchboard
(408) 431-1000

C++ Installation Support
(408) 461-9133

C++ Advisor Lines ($2.95/minute, first minute free)
DOS: 
	1-800-368-3366 (charged to a credit card)

Windows:
	1-800-782-5558 (charged to a credit card)
		
TECHFAX line for receiving technical information documents:
	1-800-822-4269 

Product Order Desk
	1-800-331-0877

Customer Service and Disk Replacement
	(510) 354-3828

Telephone Product Registration
	1-800-845-0147

C. Online services
------------------
You can find support and information online at the following 
locations:

INTERNET: Download FTP Site
	ftp.borland.com

Download Bulletin Board System
	(408) 431-5096

World Wide Web: 
	Borland Home Page
	http://www.borland.com/

	Technical Information Page
	http://www.borland.com/techsupport/borlandcpp
		
	C++ Information Page Search Page
	http://www.borland.com/techsupport/borlandcpp/search.html
		
	Bug Submission/Publication Page
	http://www.borland.com/bugs/

	Patches Available Page
	http://www.borland.com/techsupport/borlandcpp/patchs.html

	CompuServe: 
	GO BORLAND to reach all Borland pages
	GO BCPP for Language and Tools issues
	GO BCPPLIB for library-specific issues


/**************************END OF FILE****************************/
```

```
      ÜÜÜÜÜÜ   ÜÜÜÜÜÜ
      Û°ÜÜÜÛ   ÛÛÛÛÛÛ     ÜÜÛÛÛÛÛÛÛÛÛÛÛ
      Û±ÛÛÛÛ   ÛÛÛÛÛÛ   ÜÛÛÛÛÛÛÛÛÛÛÛÛÛÛ
      Û²ÛÛÛÛ   ÛÛÛÛÛÛ  ÞÛÛÛÛÛÛßßßßßßßßß
 ßÜÛÛ ÛÛÛÛÛÛ ² ÛÛÛÛÛÛ  ÛÛÛÛÛÛÜÜÜÜ ßßßßßßßßÛßß ß   ß                ß  ß ßßÛÜß
 ÜÛÛÛÜ ßÛÛÛÛÜÜÜÛÛÛÛß ÜÜ ÛÛÛÛÛÛÛÛ ÜÛÛÛÛÛÛÛÜ  ÛÛÛÛÛ ÜÛÛÛÜ ßÛÛÛÛÛÛÛ ÛÛÛÛÛÛÛÛ ÛÛÜ
Ü ßÛÛß ÜÛÛÛÛßßßÛÛÛÛÜ ßß ÛÛÛÛÛßßß ÛÛÛßßÛÛÛÛÛ ÛÛÛÛÛÛÛÛÛÛÛÛ ÛÛÛßßßß ÛÛÛßßßßß Ûß Ü
 ÜÛÛÛ ÛÛÛÛÛÛ ² ÛÛÛÛÛÛ  ÛÛÛÛÛÛ  ÛÛÛÛÛ  ÛÛÛÛÛ ÛÛÛÛÛßÛÛÛÛÛß ÛÛÛ Û ÛÛÛÛÛÜÜ ÜÛÛÛÛÜ
 ÜßÛÛ ÛÛÛÛÛÛ ± ÛÛÛÛ²Û  ÛÛÛÛÛÛ  ÛÛÛÛÛ  ÛÛÛÛÛ ÛÛÛÛÛ  ßßß ÜÛÛÛÛ ß ÛÛÛÛÛßß ßÛÛÛßÜ
      ÛÛÛÛÛÛ   ÛÛÛÛ±Û  ÛÛÛÛÛÛ  ÛÛÛÛÛÜÜÛÛÛÛÛ ÛÛÛÛÛ      ÛÛÛÛÛÜÜÜÜ ÛÛÛÜÜÜÜÜ
      ÛÛÛÛÛÛ   ÛÛÛÛ°Û  ÛÛÛÛÛÛ   ßÛÛÛÛÛÛÛÛß  ÛÛÛÛÛ       ßÛÛÛÛÛÛÛ ÛÛÛÛÛÛÛÛ
      ÛÛÛÛÛÛ   ÛÜÜÜÜÛ                                           ASCii<ROY>

                              
                               P R E S E N T S


ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
³                                                                            ³
³                         BORLAND C++ RELEASE 5.02                           ³
³                                                                            ³
ÀÂÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÂÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÂÙ
 ³ Type..........: PROGRAMING         ³ Packager......: STINGRAY.Zero       ³
 ³ Publisher.....: BORLAND            ³ Cracker.......: /                   ³
 ³ Supplier......: TEAM XFORCE        ³ Release Date..: 05/07/97            ³
 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÁÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ

ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
³  Release notes..                                                           ³
ÀÂÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÂÙ
 ³                                                                          ³
 ³                                                                          ³
 ³  Compiler Enhancements                                                   ³
 ³  ---------------------                                                   ³
 ³  New 32-bit compiler (BCC32.EXE) provided with this release              ³
 ³  A Make following a failed Build All rebuilds from the point of failure  ³
 ³  New compiler option under Options|Project|C++ Options|                  ³
 ³  General called Zero-Length Empty Class Member Function (like -Vx)       ³
 ³                                                                          ³
 ³  Editor Enhancements                                                     ³
 ³  -------------------                                                     ³
 ³  Read-only files identified by an "R" after the file name                ³
 ³  Search|Replace includes a Change All option                             ³
 ³  IDE remembers the cursor position of the last 100 edit buffers that     ³
 ³  you closed                                                              ³
 ³  IDE automatically loads the Tips script to display tool tips            ³
 ³  Cursor changes in left gutter to indicate that a click will drop        ³
 ³  a debugger breakpoint                                                   ³
 ³                                                                          ³
 ³  Debugging Enhancements                                                  ³
 ³  ----------------------                                                  ³
 ³  New options in Options|Environment|Debugger|Debugger Behavior:          ³
 ³  Do not save files or prompt when debugging and Do not prompt            ³
 ³  when attempting to run 16 bit applications                              ³
 ³  New option in Options|Project|Compiler|Debugging:                       ³
 ³  Debugger status glyphs: Lightning bolt (if running) and Pause Process   ³
 ³  (if stepping or at breakpoint)                                          ³
 ³  Debug menu: View Locals command creates Local Inspector (to watch local ³
 ³  variables) when the IDE Debugger has a process loaded                   ³
 ³  The Watch window shows values in hex, decimal, or both formats          ³
 ³  CPU View stack pane indicates the current position                      ³
 ³  While debugging, editor tooltips display the value of the symbol        ³
 ³  under the pointer                                                       ³
 ³                                                                          ³
 ³  And a lot more ...                                                      ³
 ³                                                                          ³
 ³  INSTALLATION: unrar and run SETUP.EXE                                   ³
 ³  -------------                                                           ³
 ³                                                                          ³
 ³  When so many groups bring you crap fakes non-working, X-FORCE always    ³
 ³  gets you the Best of the Best. ACCEPT NO IMITATION !                    ³
 ³                                                                          ³
 ³                                                        X-Force 1997! gNx ³
 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
                                                                        
ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
³   Group News & Greetings..                                                 ³
ÀÂÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÂÙ
 ³                                                                          ³
 ³                                                                          ³
 ³  OUR DiAMONDS-4-EVER GREETiNGS MUST GO TO :                              ³
 ³                                                                          ³
 ³  Stingray , Mach One , Ones Wally , Slain , Wildchild , Roamer           ³
 ³  BlackMagic , Wayward , The Riddler , Longshot , SWC , Dim               ³ 
 ³  Blueyes, Winterhawk, Solar and the ones who deserve it ...              ³
 ³                                                                          ³
 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ

ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
³  The loyal ones..                                                          ³
ÀÂÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÂÙ
 ³                                                                          ³
 ³                                 LEADERS                                  ³
 ³                ÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ                 ³
 ³                    MACH ONE - ONES WALLY - STINGRAY                      ³
 ³                                                                          ³
 ³                                                                          ³
 ³                                 SENIORS                                  ³
 ³                ÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ                 ³
 ³                    KAPITANO - MR SAINT - THE RIDDLER                     ³
 ³                                                                          ³                                                                          ³
 ³                                                                          ³
 ³  Bugs Bunny - Defiance - Doze - Roamer - Prodigal - Gahn - Dim - Dagobah ³
 ³  Hawk - Mr BlazerYumYum - Alpha - Tgf - Regor - Bate - Saturn - Merlin   ³
 ³  ShadowSeeker - Old El Paso - Black Bull - Abrasax  - Utopian - Blueyes  ³
 ³    ADC - Twizted - Leduke - Saturn - Brush - Mampy - Deepmind - Sledge   ³
 ³                                                                          ³
 ³   Cruger - Fronthead - Skylord - Hurricane - MGD - Sniper - Dark Druid   ³
 ³                                                                          ³
 ³                                                                          ³
 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ

                       * all sysops are full members *

ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
³  Famous X-Force boards around the globe..                                  ³
ÀÂÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÂÙ
 ³                                                                          ³
 ³ ANOTHER WORLD          WORLD   HEADQUARTERS   Xxxxxxx         xx LINES   ³
 ³                                                                          ³
 ³ The Ghetto             USA     Headquarters   Andeveron       10 Lines   ³
 ³ Strawberry Fields      EURO    Headquarters   Deuteros        10 Lines   ³
 ³ Maximum Security       CANADA  Headquarters   Darkwave         5 Lines   ³
 ³ Vax Museum             SPAIN   Headquarters   Ones Wally       6 Lines   ³
 ³                                                                          ³
 ³ Exxxxx                 X-Force Ftp WORLD   HQ Xxxxxxx         50 Lines   ³
 ³ Dxxxxx                 X-Force Ftp USA     HQ Xxxxxxx         50 Lines   ³
 ³ Sxxxxx                 X-Force Ftp EURO    HQ Xxxxxxx         50 Lines   ³
 ³ Sxxxxx                 X-Force Ftp COURIER HQ Xxxxxxx         50 Lines   ³
 ³ Axxxxx                 X-Force Ftp MEGA    HQ Xxxxxxx         50 Lines   ³
 ³ Txxxxx                 X-Force Ftp SUPER   HQ Xxxxxxx         50 Lines   ³ 
 ³ Hxxxxx                 X-Force Ftp MEMBER     Xxxxxxx         50 Lines   ³ 
 ³                                                                          ³
 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
                                      
ÚÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄ¿
³  How to reach us..                                                         ³
ÀÂÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÂÙ
 ³                                                                          ³
 ³ If you think you should be in the .nfo but you are not, please call up   ³
 ³ a HQ and leave a message to a senior member , or just join the channel   ³
 ³ #x-force on irc.                                                         ³
 ³                                                                          ³
 ÀÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÄÙ
  
 [-----------------  X-FORCE 1997 SMOKING THE COMPETITION  --------04/25/97-]
```
