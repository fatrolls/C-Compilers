                **************************************
                 WELCOME TO TURBO C++ FOR WINDOWS 4.5
                **************************************

This README file contains important information about TURBO
C++ FOR WINDOWS 4.5 (TCW).  For the latest information
about TCW and its accompanying programs, read this entire
file.

*****************
TABLE OF CONTENTS
*****************
1.  How to Get Assistance
          -- Sources of information
2.  Installation
          -- Installing Turbo C++ on your hard disk
3.  New Features
4.  Important Information
          -- Acrobat Reader 2.0
          -- Importing Project Files from Borland C++ 4.x
          -- Quick Tour Help file
          -- ObjectComponents Framework (OCF), OLE 2.0, and ObjectWindows 2.5
                   -- Registering debugging versions of OLE servers under TCW
                   -- New file in WINDOWS\SYSTEM directory
                   -- New tools for registering OLE servers and
                      automation controllers
                   -- Debugging OLE applications under Windows NT
                   -- WinSight
                   -- OLE error codes
                   -- OLE2 applications
                   -- OLE implementation under Windows NT
                   -- OLE2 compiler options
          -- VBX Support 
          -- VBX Controls Included with TCW
          -- OpenHelp
                   -- OpenHelp with TASM 
          -- Limitation in DOCVIEW.IDE
          -- DDVT functions and RTTI
          -- Inline assembly and interrupts
          -- Creating 16-bit import libraries from .DEF files
          -- New Compiler Switches 
          -- NOEHxx Libraries
          -- IDE/Integrated Debugging
          -- InProc servers and the IDE
          -- Using Tools with NTFS
          -- Running from a Windows 3.1 DOS Prompt
          -- Converting TCW 3.1 to TCW 4.5 code
          -- Floating-Point Formats
          -- AppExpert and OWL
          -- C/C++ Language Features


*********************************************
1. HOW TO GET ASSISTANCE
*********************************************
If you have any problems, please read this file, the
HELPME.WRI and other files in your DOC subdirectory, and
check the on-line help. 

*********************************************
2. INSTALLATION 
*********************************************
IMPORTANT!

Do not install TCW 4.5 over previously installed TCW directories. The
files in this distribution will not work with tools and libraries
shipped before BCW 4.5 and TCW 4.5.

If you used Turbo Assembler 4.0 with a previous installation of TCW,
you must reinstall it after installing TCW 4.5.

Also, be especially careful when using object files and libraries
from earlier TCW versions with binaries created with this
release. There are several potential problems when linking with old
objects or libraries. Exceptions won't work correctly (destructors won't
get called) when a pre-BC4 stack frame is unwound due to an exception.

Do not use long file names when installing under Windows NT.

-----------------------------------------------
Installing TCW 4.5 on your hard disk
-----------------------------------------------

Diagnostic and debug version of OWL are not installed to the hard
disk, but they can be copied from the CD.  

Users of ObjectWindows 1.0, should read the COMPAT.TXT file for
compatibility information.

**** Note to Windows NT, OS/2, and Windows 95 users **** 

If you intend to use TCW under any of these platforms you must
follow some additional installation steps, which are listed in
the INSTALL.TXT file.  If you fail to read and follow these
configuration guidelines, you may encounter several significant
problems when using TCW.

For more information about installing and configuring TCW, see the
file INSTALL.TXT which can be found in the following locations:
* TCW CD-ROM (\TCWIN45\INSTALL.TXT)


***************
3. NEW FEATURES
***************
TCW 4.5 includes the following new features:

OLE SUPPORT:
  - A complete encapsulation of OLE2 via new ObjectWindows classes
    and the ObjectComponents Framework, a new set of C++ classes. This
    allows you to develop applications that support the following
    16-bit OLE capabilities:
          * Linking and embedding containers
          * Linking and embedding servers
          * Automation servers (automatable servers)
          * Automation controllers
          * OLE clipboard operations
          * OLE drag and drop operations
          * In-place editing
          * OLE user interface, including menu merging, pop-up menu
            for activated object, verbs on container's Edit menu
          * Compound file storage
          * Registration
          * Localized strings for international support
          * Type libraries
  - New utilities to make OLE programming easier:
          * WinRun allows you to launch Window application from the 
            MS-DOS prompt in Windows 3.1.  (See UTILS.TXT for
            more information.)
          * AutoGen, MacroGen, GuidGen produce helpful class
            declarations, macro,s and OLE identifiers automatically
          * DllRun and Register simplify running and testing DLL
            servers
  - IDE enhancements to TargetExpert, AppExpert, and ClassExpert to
    support the new OLE2 capabilities.

    
COMPILER FEATURES
  - Support for ANSI C++ exception handling, structured exception handling
    under C, and mixed C/C++ exception handling. 
  - Support for ANSI C++ operator new[] and operator delete[].
  - Runtime Library support for the ANSI C++ string class.
  - Support for ANSI C++ runtime type identification (RTTI).
  - Support for ANSI C++ new style casts dynamic_cast, static_cast, const_cast,
    and  reinterpret_cast.
  - Support for three character types as provided in ANSI C++.

LINKER FEATURES
  - Linker debug capacity expanded.

IDE FEATURES
  - Integrated GUI debugging for 16-bit Windows applications.
  - A new project manager that supports multiple targets, drag-and-drop,
    and Style Sheets for associating options.
  - AppExpert, which simplifies the process of creating
    ObjectWindows applications through code generation.
  - ClassExpert, which simplifies adding and managing classes in
    your AppExpert application.
  - Transfers, Settings Notebook, SpeedMenus, and a configurable SpeedBar.
  - Expanded editor support, including column blocking and window
    splitting.  TEMC now called KEYMAPR.

RESOURCE WORKSHOP
  - Resource preview
  - DialogExpert
  - Auto ID numbering
  - Auto mapping of accelerators and help hints to menu items
  - Support for VBX controls
  - SpeedMenus
  - Dialog editor property inspector
  - Integrated with ClassExpert and IDE project manager

OBJECTWINDOWS LIBRARY (OWL)
  - Complete coverage of Windows API, including GDI
  - Single source for Win 3.1, Win 32s, and NT 
    (building 32-bit applications requires Borland C++)
  - Built in exception handling using standard C++ exceptions for robust error
    handling
  - Built-in type safety using standard C++ templates
  - Toolbars, status lines, and print preview
  - Flexible Document/View architecture
  - Supports VBX 1.0 controls in a dialog or window
  - Layout Windows
  - Mix-in architecture
  - Support for 3d controls
  - Support for BWCC controls
  - Gadgets and Widgets
  - Printing and print previewing support

GAME EXAMPLES
  - Five new sample programs:

      EXAMPLES\OWL\GAMES\BLAKJACK
                        \BLOCKS
                        \CRIBBAGE
                        \METEOR
      EXAMPLES\WINDOWS\MAHJONGG

DOCUMENTATION FEATURES
  - OpenHelp, a utility that enhances the functionality of Windows Help
    by allowing you to quickly search for topics across Help files, as
    well as the ability to add your own Help files (or remove them) from
    the search.
  - Documentation in the Acrobat 2.0 document viewing browser.
    Acrobat lets you search through the entire documentation set to find 
    selected topics.  You can view the contents page by page and
    print sections of particular interest.  

VBX SUPPORT
  - Borland's visual tools, such as Resource Workshop, provide
    support of VBX 1.0 controls via a DLL called BIVBX11.DLL. You can
    freely distrubute this DLL with programs you create that use VBX
    controls.

BIVBX11.DLL has been tested with a large number of VBX controls written to
the Microsoft Visual Basic 1.0 CDK specification. If you have a problem with
a specific control, make sure that it does not require VB 2.0 or VB 3.0 CDK
functionality. VBX 2.0 and 3.0 controls will usually display a message saying
that they require VB 2.0 or 3.0 support. In some cases, though, the control
may appear to work but exhibit instability. Please contact the control vendor
and explain the problem. They may have an updated control or may be able to 
contact Borland to find a solution.


************************
4. IMPORTANT INFORMATION
************************
This section contains important information not found elsewhere in
the product documentation. Please read through this material
in its entirety.

------------------
Acrobat Reader 2.0
------------------

The four books available online duplicate material
already in the online Help.  We recommend using the Acrobat
Reader to read long sequences of material in order and
the online Help when searching for specific information by
keyword.  

The Acrobat Reader is capable of high-quality printed
output.  You might prefer to print sections of the manuals
that you use frequently.

--------------------------------------------
Importing Project Files from Borland C++ 4.x
--------------------------------------------

When TCW loads an .IDE file created with Borland C++, it
shows a dialog box warning that the project might contain
target types and option settings that TCW does not
support.  If you click Yes to import a BC project, TCW
ignores any optimization settings the project might
contain.  The TCW project manager displays DOS targets and
Win32 targets, but attempting to build them causes errors.

For more details about what project features might
cause problems for TCW, click the Help button in the
warning dialog box.

You can disable the dialog box, if you prefer, with the
following setting in your TCW.INI file.

    [Project]
    ImportBorlandIDEFile=1

With this setting, TCW automatically converts any .IDE
file without warning.

Borland C++ reads TCW .IDE files without difficulty.

TCW 4.5 does not support development of OWL 1 applications.
The differences between OWL 1 and the current OWL 2.5 are
large enough to render them incompatible. You will need to
convert your OWL 1 programs to use OWL 2.5 before you can
build them.  For help converting, see Appendix A of the
ObjectWindows Programmer's Guide in the online
documentation.

--------------------
Quick Tour Help File
--------------------

To get you started quickly with using Turbo C++ for Windows, take
a look at the online Quick Tour. The Quick Tour provides an
overview of the product, with animated demonstrations of its many
features.

System Requirements
-------------------
Although you can view the Quick Tour at any screen resolution, a
resolution of at least 800 x 600 is recommended.

Installation Notes
------------------

If you choose to install the Quick Tour Help file, then you
also need to run Microsoft's Setup program for Video for
Windows. Normally the TCW install launches Setup for you
automatically.  If you have chosen the WinLAN
configuration, however, then a system administrator will
have to run the Video for Windows Setup program for you
because Setup writes to the system registry.

Without Video for Windows, the Quick Tour Help file cannot
play animation sequences.

The animation (AVI) files are stored on the CD and are not
automatically installed on your hard drive. For this reason, you
need to leave the CD in the drive while viewing the Quick Tour if
you want to view the demonstrations. If the CD is not in the
drive, an error message is displayed when you try to run a
demonstration.

Although compression of the animation files is optimized to run
from the CD-ROM, you can also run them from your hard drive. To
do so, you need to make the following changes:

1. Create a directory called AVI under the TCWTOUR directory
   located in your Turbo C++ for Windows directory (TCWIN45, by
   default).

2. Copy all the files from the \TCWIN45\TCWTOUR\AVI directory on
   the CD-ROM to the \TCWTOUR\AVI directory on your hard disk.

3. In WINHELP.INI, change the value of CdTcPath so it points to
   the drive and directory in which you installed TCW. If you
   used the default directory (TCWIN45), you will only need to
   change the drive letter to that of the hard drive where TCW is
   installed.

The Quick Tour page that describes features for
internationalizing applications allows you to launch the
INTLDEMO example program directly from the Help file.  If
you chose not to install the Borland custom control library
(BWCC.DLL) then INTLDEMO.EXE cannot run.


Starting the Quick Tour
-----------------------
You can start the Quick Tour from the following places:

- From the Quick Tour icon in the Turbo C++ 4.5 desktop group.

- From the Quick Tour button in the About Turbo C++ dialog box
  which displays the first time you start the IDE.

- From the Quick Tour command on the Help menu.

Uninstalling the Quick Tour
---------------------------
You can uninstall the Quick Tour after viewing it by deleting the
TCWTOUR directory located under the directory where you installed
Turbo C++ for Windows (TCWIN45, by default).

----------------------------------------------------------------
ObjectComponents Framework (OCF), OLE 2.0, and ObjectWindows 2.5
----------------------------------------------------------------

Registering debugging versions of OLE servers under TCW
-------------------------------------------------------
The debugger, debugid, and debugdesc registration keys require
the use of a debugger that can be invoked from the command line.
Turbo C++ for Windows 4.5 does not provide a command-line debugger.
You can purchase Turbo Debugger for Windows as part of the
Borland TASM assembler product.


New file In WINDOWS\SYSTEM directory
-------------------------------------
TCW 4.5 installs a new file called BOCOLE.DLL in your
WINDOWS\SYSTEM directory. This library must be present in order for any
ObjectComponents program to execute.

Debugging OLE applications under Windows NT
-------------------------------------------

When debugging OLE applications under Windows NT 3.5, you may experience
a lock up if a program is forced to terminate.  This will happen when any
OLE application is running under the IDE and you explicitly request
Debug | Program Terminate, or implicitly request program termination by
closing a project.  This problem will not occur under Windows 3.1 or Windows
95, and will not happen with non-OLE applications.  Borland recommends that
all developers running under NT accept any updates to the NT OLE DLLs if and
when they are made available by Microsoft.

WinSight
--------
When WinSight spies on an ObjectWindows OLE container, it sometimes causes
corruption of the container's menus.  This behavior is expected.  If it
occurs, quit the application and start again.

OLE error codes
---------------
The file DOC\OLE_ERRS.TXT contains a list of the error codes OLE defines.
The list is sorted in numerical order.  Refer to it for help in interpreting
OLE-related error returns.

OLE2 applications
-----------------
Many commercial products are now offering their first generation of OLE2
enabled applications. Some of these applications are more complete
OLE implementations than others. Borland has observed several major
commercial applications that exhibit errant behavior when asked to
perform certain OLE operations. This is especially true when asked to
embed DLL servers, which many OLE applications appear to be
unprepared to handle. If you experience problems when using OLE
applications you create with TCW in conjunction with third party
products, do not jump to the conclusion that the problem is yours.  Until 
OLE applications in the market place mature, it is not yet a safe assumption
that just because a product comes from a leading company that it is
robust. Changes introduced between OLE 2.0 and OLE 2.02 are
responsible for exposing some of these problems. When reporting bugs
in OLE applications to third parties, be sure to specify that they should
be developing and testing under the latest version of OLE.

OLE implementation under Windows NT
-----------------------------------
The 16 bit OLE implementation originally shipped in Windows NT 3.5 may
exhibit problems with DLL servers and may behave differently than the
version of OLE that MS recommends for Windows 3.1. Borland
recommends that all NT developers update to later versions of the NT OLE
DLLs if and when they are made available by Microsoft.

OLE2 compiler options
---------------------
When linking 16 bit OLE2 modules, the OLE2 import library
(ole2w16.lib) must come before the RTL import library (import.lib.)


-----------
VBX Support 
-----------
The BIVBX102.DLL has been renamed to BIVBX11.DLL.

BIVBX11.DLL has been tested with a large number of VBX controls written
to the Microsoft Visual Basic 1.0 CDK specification. If you have a problem
with a specific control, make sure that it does not require VB 2.0 or
VB 3.0 CDK functionality. VBX 2.0 and 3.0 controls will usually display a
message saying that they require VB 2.0 or 3.0 support. In some cases,
though, the control might appear to work but exhibit instability. Please
contact the control vendor and explain the problem. They might have an
updated control or might be able to contact Borland to find a solution.

The following functions in BIVBX.H are limited to 16-bit only. To
allow for portability to 32-bits, these functions should be replaced
as follows:

 Old (16-bit only)         New (16-bit and 32-bit)
 -----------------         -----------------------
 VBXGetBasicStringPtr      VBXGetBasicStringBuf
 VBXGetCStringPtr          VBXGetCStringBuf
 VBXGetEventName           VBXGetEventNameBuf
 VBXGetPropName            VBXGetPropNameBuf
 VBXLockCString            VBXLockCStringBuf
 VBXMethod                 N/A

Turbo C++ 4.5 does not support 32-bit development, but using the more
portable names is still a good idea in case you later upgrade to
Borland C++ and want to create a 32-bit application.

For more information, see the BIVBX.WRI file.

TargetExpert now manages libraries for VBX controls.   If you have an IDE
project which uses VBX controls, make the following change  to your project
to take advantage of TargetExpert support:
- In the project window, delete the bivbx.lib node.
- In the project window, right click on your EXE node.
- From the resulting SpeedMenu, select TargetExpert.
- In TargetExpert, enable the VBX checkbox and press OK.

------------------------------
VBX Controls Included with TCW
------------------------------

If you choose to install the example programs, TCW places a
set of VBX controls in your WINDOWS/SYSTEM directory.  The
VBX controls are made by MicroHelp.  Two of the examples,
Turbo MahJongg and TurboCribbage, make use of one of the
MicroHelp VBX controls

For more information about what controls are included
and how to use them, find the Help file called VBT300.HLP
in your BIN directory.

To find out more about using VBX controls generally
with Turbo C++, consult the online Help and the
ObjectWindows Programmer's Guide in the Acrobat Reader.   

----------
OpenHelp
----------
See the online Help provided with OpenHelp (OPENHELP.HLP) for details on how
to use and configure this new search engine.

OpenHelp with TASM 
------------------
If you install TASM with TCW4.5, you need to run the OpenHelp configuration
to configure your Help files. 

-------------------------
LIMITATION in DOCVIEW.IDE
-------------------------

The OWL example called DOCVIEW has a project file called
DOCVIEW.IDE. The project file has a number of different
target nodes. The best way to build all the nodes
successfully is to use the Project|Build All command. There
is a potential danger because many of the products produce
intermediate .OBJ files with the same name, but the .OBJs
are compiled differently.  Using a Make command, one node
might end up accidentally using and .OBJ that was built for
a different node.

-----------------------
DDVT functions and RTTI
-----------------------
When compiling code that contains DDVT functions, do not use run-time type
information or you will receive an error message. In order to compile
without using run-time type information, compile all code that uses DDVTs
(for instance OWL 1.0x libraries and applications)with the -RT- switch
(Options|Project|C++ Options|Exception handling\RTTI in the IDE).

------------------------------
Inline assembly and interrupts
------------------------------
If your inline assembly code includes an interrupt call, the compiler does
not preserve any registers altered by the call. You must write code to save
and restore registers when using interrupt calls within inline assembly
code.

---------------------------------------------
New Compiler Switches and Linker Optimizations
----------------------------------------------
See your documentation for a description of the new compiler switches
for exception handling.

----------------
NOEHxx Libraries
----------------
Purpose:

The NOEHxx libraries eliminates the overhead of exception-handling code in
the run-time library for users who don't need it and who do rely on any
libraries that require it.

How to use:

A NOEHxx library must be linked in before the standard runtime library.

For the IDE, add the approriate library to the project using AddNode.
To ensure the NOEHxx library is processed before the standard libraries,
turn on "Show Runtime Nodes" in the Options|Environment|ProjectView dialog.
From the project window you can move the library up and down using the
ALt-<arrow> keys. Be sure the NOEHxx library appears before other standard
libraries. 

What they do:

The NOEHxx libraries resolve calls to exception-related compiler helper
functions to dummy functions that return appropriate return values. They
also restore the pre-exception behavior of operator new to return NULL on
out of memory conditions. Non-exception enabled versions of setjmp() and
longjmp() are also provided.

Limitations:

Note: some new features (first introduced in Borland C++ 4.0) require
exception handling.  These include the string class, BIDS container
classes, the standard OWL libraries, and RTTI.

------------------------
IDE/Integrated Debugging
------------------------
Using the Microsoft DBWIN utility interferes with the Event log's ability to
display those same messages. To see those messages in the Event log, either
quit DBWIN or select Options|No Output in DBWIN.

DDE applications must be debugged in hard mode.

Hard-mode debugging does not work reliably under Windows NT version 3.1,
and might crash the WOW session. The IDE disallows users from selecting
hard mode on all stops, but setting a breakpoint on certain Windows
messages might cause the debugger to go into hard mode.

---------------------
Using Tools with NTFS
---------------------
16-bit tools running on NT cannot use NTFS filenames.

-----------------------------------------------------------
Converting TCW 3.1 Windows Code to TCW 4.5
------------------------------------------------------------
To get your TCW++ 3.1 code to compile and run under TCW 4.5, modify
your code to reflect three character types where compiler errors
occur when using the TCW 4.5 RTL includes.  Alternatively, you can
set a compiler option and use the RTL includes from TCW 3.1.  The
option you need to set is

   Options | Project | C++ Options | Compatibility | 
   'Do not read 'char' as distinct type'

This option provides for only two character types. Also, use operator
new[]() and delete[]() syntax for class arrays.

----------------------
Floating-Point Formats
----------------------
Floating-point formats are a collection of formatting information used to
manipulate floating point numbers in certain runtime library functions such
as scanf() and atof().

This section discusses why you might get the error
FLOATING POINT FORMATS NOT LINKED : ABNORMAL PROGRAM TERMINATION and tells
you how to resolve it.

There are no current plans to fix this because it is not a bug. The
intent is to avoid linking the floating-point formats (about 1K of
overhead) when they are not required. The tradeoff is that the
programmer must explicitly request that the floating-point formats be
linked in for some programs that manipulate floats in a limited and
specific fashion.

Because you can get this error in a number of different ways, check the
following list of potential causes to find out how to resolve the error.
The causes are listed in order of most common to least common.

  1.  CAUSE:  Floating point set to <None>.  You have your
      floating point option set to None when it should be set to
      either Fast or Normal.

      FIX:  Set Floating Point to Fast or Normal.

  2.  CAUSE:  Either the compiler is over-optimizing, or the
      floating-point formats really do need to be linked in because
      your program manipulates floats in a limited and specific
      fashion. Under certain obscure conditions, the compiler will
      ignore floating point usage in scanf() (e.g., trying to
      read into a float variable that is part of an array contained
      in a structure.)

      FIX: Add the following to one source module:

           extern _floatconvert;
           #pragma extref _floatconvert

  3.  CAUSE:  Forgetting to put the address operator & on the scanf
      variable expression. For example,
       float foo;
       scanf("%f", foo);

      FIX: Change the code so that the & operator is used where it
      is needed.  For example, the above code should be
       float foo;
       scanf("%f", &foo);

-----------------
AppExpert and OWL
-----------------

If you are bringing programs from Borland C++ 4.x into TCW 4.5:  the
value of the IDS_LISTNUM define in OWL has changed since BC++ 4.02. 
If you have created an application in BC++ 4.0 or 4.02 using
AppExpert, you will receive redefinition warnings when rebuilding in
TCW 4.5.  To correct this problem, update the .RH file for your
project to match the new value for this define.  Specifically, the
following line

    #define IDS_LISTNUM 32582

should be changed to

    #define IDS_LISTNUM 32584

----------------------
C/C++ Language Changes
----------------------
Many changes were made to the compiler in compliance with the
latest changes proposed by the ANSI C++ committee.  These include
three distinct char types, enhancements to templates, support for
virtual functions differing in return types, and other improvements
listed here.  See the Library Reference and the Programmer's Guide
for complete details on these changes and how they affect your
code.

wchar_t is a fundamental data type in C++ programs. In C programs it
continues to be a typedef defined in stddef.h. See online Help.

Enum operator overloading is also supported.

The runtime library now supports the ANSI C++ string class.  If you
already have a string class, it must be renamed for Turbo C++ 4.5.

In addition, operator new and operator new[] now throw an
exception (xalloc), as specified by the ANSI C++ committee.
To get the old behavior, you can issue set_new_handler(0). 
(set_new_handler(0), however, does not work with ObjectWindows
or string classes.) See Chapter 3 of the Programmer's Guide.

Arrays are now being allocated through operator new[]() and deleted
by operator delete[](). An example is provided in Chapter 3 of the
Programmer's Guide.

Turbo C++ 4.5 implements ANSI C++ runtime type identification (RTTI).
See the Library Reference, "C++ runtime support",  for a description
of class Type_info. RTTI and operator typeid() are fully described in
Chapter 3 of the Programmer's Guide.

Turbo C++ provides a full implementation of exception handling
under C++ and C.  C exceptions can be handled in C or C++ code;
C++ exceptions can be handled only in C++ code. The C++ exceptions are
described in the Library Reference, "C++ run-time support." See Chapter 4
of the Programmer's Guide for a full description of how to use exception
handling.

Turbo C++ 4.5 also implements the accepted ANSI C++ new style casts.
See the Chapter 3 of the Programmer's Guide for information and
examples.
