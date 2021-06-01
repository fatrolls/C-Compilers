/*****************************************************************/
                  Welcome to Borland C++ Release 5.02
------------------------------------------------------------------

This README file contains important information about Borland C++.
For information about OWL updates, see \BC5\DOCS\OWL5.TXT.

--------
CONTENTS
--------
* Contacting Borland
* Online Licenses
* Redistributable Files List
* New IDE Features
* Incremental Linker
* Interoperability with Borland C++Builder
* New Scripting Features
* New Resource Workshop Features
* Issues

------------------
Contacting Borland
------------------

Borland offers a range of services to provide comprehensive 
product information, updates, and product services. You can 
get more information on Borland C++ by contacting any of 
these resources:

World Wide Web:  http://www.borland.com/

Tech Info page:  http://www.borland.com/TechInfo/

FTP:             ftp.borland.com

Up & Running:    (408) 461-9133 (Installation support)

Listserv:        listserv@borland.com
Send an email message containing this text:

  SUBSCRIBE<space>BCPP<space>FIRSTNAME<space>LASTNAME

---------------
Online Licenses
---------------

Borland now provides the software license online. Refer to 
the file license.txt in the root directory of the CD for details.

--------------------------
Redistributable Files List
--------------------------

Refer to the file redist.txt for a list of redistributable 
files for Borland C++ 5.02.

----------------
New IDE Features
----------------

The IDE includes many usability enhancements in this release.
They are listed briefly in the following sections. Refer to 
online Help for details.

Compiler Enhancements
---------------------

* New 32-bit compiler (BCC32.EXE) provided with this release

* A Make following a failed Build All rebuilds from the point 
  of failure 

* New compiler option under Options|Project|C++ Options|
  General called Zero-Length Empty Class Member Function (like -Vx)

Editor Enhancements
-------------------

* Read-only files identified by an "R" after the file name

* Modified files include an asterisk (*) after the file name

* Search|Replace includes a Change All option

* IDE remembers the cursor position of the last 100 
  edit buffers that you closed 

* IDE automatically loads the Tips script to display tool tips

* Cursor changes in left gutter to indicate that a click 
  will drop a debugger breakpoint

Debugging Enhancements
----------------------

* New options in Options|Environment|Debugger|Debugger Behavior:
  Do not save files or prompt when debugging and Do not prompt
  when attempting to run 16 bit applications

* New option in Options|Project|Compiler|Debugging:
  Detach Debug Information from OBJs

* Debugger status glyphs: Lightning bolt (if running)
  and Pause Process (if stepping or at breakpoint)

* Debug menu: View Locals command creates Local Inspector (to 
  watch local variables) when the IDE Debugger has a process loaded

* The Watch window shows values in hex, decimal, or both formats

* CPU View stack pane indicates the current position

* While debugging, editor tooltips display the value of the symbol
  under the pointer

Message Window Enhancements
---------------------------

* An .RC file's source date and time format 
  reflect the format of the country setting

* The default position of the Message window has changed

* You can use Ctrl+ A to clear the Build tab

* Clear before Make/Build in Options|Environment|Preferences

* Double-click on an unresolved external error message 
  in the Build tab opens the file with the external reference

Project Management Enhancements
-------------------------------

* Project menu: Stop Background Task appears during an 
  asynchronous build 

* Project window glyphs: A red check mark (node has 
  Local Overrides) and a clock with a red X on it 
  (node out of date and will be rebuilt on the next make)

* The default position of the Project window has changed

* Compatibility: Two new Project Options on the C++ Options|C++ 
  Compatible dialog, Destructor Cleanup Compatibility and Class 
  Layout Compatibility

General Enhancements
--------------------

* Preprocessor: Invoking the preprocessor automatically loads
  the output into the edit buffer

* Syntax highlighting: Scope delimiters ) and } can be 
  customized; preprocessor directives highlighted only 
  instead of highlighting the whole line

* File|Open dialog boxes: Enable filename completion 
  available in Options|Environment|Preferences for files 
  and directories

* Keyboard Shortcuts: You can use Ctrl+S to find the ~, <, and > 
  characters 

* Windows NT: Shutting down the computer now saves an open 
  .IDE file. 

------------------
Incremental Linker
------------------

Borland C++ provides an incremental linker that dramatically improves 
link times (after the initial link). To use it, check Incremental 
Linker on the Options|Project|Linker|32-bit Linker page. 

----------------------------------------
Interoperability with Borland C++Builder
----------------------------------------

If you have Borland C++Builder, you can add the C++Builder .MAK 
makefiles as nodes to your BCW projects. Refer to BCW.HLP for
more information.

----------------------
New Scripting Features
----------------------

* File maintenance/navigation script (DIRVIEW.SPP)

* New method ProjectStopBackgroundTask() to terminate 
  asynchronous build/make/compile/transfer

* remove_view_menu_item function in MENUHOOK.SPP lets you 
  remove IDE main menu items 

* SearchAll hot key changed from A to L. 
  (A clears the Message tab.) 

------------------------------
New Resource Workshop Features
------------------------------

* 32-bit custom control DLL support in 
  Options|Environment|Resource Editors|Control Libraries

* New menu command Dialog|Resize to Content

* Dialog editor enhancements

* Check for Duplicate ID on the Dialog menu 

* Dynamic IDE status bar 

* Entry of DBCS characters in the menu editor 

* Code page support in Resource compiler through -c switch 
  and #pragma code_page(ID-num)

------
Issues
------

New 32-bit Compiler Rule
------------------------

The new 32-bit compiler implements a language requirement that may
break some existing code. The new rule is that you cannot pass a
temporary variable by reference--you must pass it by const reference.

For example, given a function with this prototype:

  func1 (TMyClass& o);

the following call used to be acceptable:

  func1 ( TMyClass() );

However, you must now change the call to:

  func1(TMyClass const & 0)

Some of the OWL examples have not been updated for this new change. 

Command-Line Options
--------------------

The command line compiler creates multithreaded applications
by default. The -WM option is on by default.

If using the -i and -s command-line options together, note that the -i
must precede the -s to work properly.

Compiler/Linker Errors
----------------------

If you receive the following compiler and linker error messages
when you compile from the command line:

Error: Unresolved external 'TApplication::Dispatch(TEventHandler::TEventInfo&,int,long)'
   referenced from module GDIDEMO.CPP
Error: Unresolved external 'TWindow::Dispatch(TEventHandler::TEventInfo&,int,long)'
   referenced from module GDIDEMO.CPP

it most likely means you are compiling as a multithreaded application,
but are linking with the single-threaded OWL libs. This is because
multithread is now the default application type. To remedy this, 
add -WM- to your options to turn multithreaded targeting off.

Restricted Keywords
-------------------

The following keywords are reserved for use in Borland C++Builder:

__automated
__classid
__closure
__dispid
__property
__published

Don't use these in your Borland C++ programs.

Multiple Declarations for HSZ
-----------------------------

If the error Multiple Declarations for HSZ is displayed, you need to 
edit \BC5\INCLUDE\WN32\DDEML.H and include the following statement:

  #define __DDEML_H

STL Stack
---------

Although unlikely, if you want to use a stack of vectors of bools,
you must define the following before any of the header files:

  #define RWSTD_NO_BOOL

------------------------
OpenHelp 6.0 Upgrade Kit
------------------------
The OHELP60 directory on the CD contains files that let you upgrade
to OpenHelp 6.0. If you have C++Builder installed on the same computer
as Borland C++, you already have OpenHelp 6.0. In this case, the upgrade
merges the Borland C++ and C++Builder OPENHELP.INI files.

See OPENHELP.HLP for information on using OPENHELP 6.0.

Upgrading to OpenHelp 6.0
-------------------------
  If you have only Borland C++ on your computer
  ---------------------------------------------
  Run OHELPNEW.BAT. This batch file takes one parameter: The parameter 
  specifies the drive and directory in which BC5 is installed. Enter a 
  colon with the drive letter, followed by the backslash and directory 
  name, e.g. C:\BC5
  Example: OHELPNEW C:\BC5
 
  If you have Borland C++ and C++Builder on your computer
  -------------------------------------------------------
  Run OHELPRPL.BAT. This batch file takes two parameters: The first 
  parameter specifies the drive and directory in which BC5 is installed. 
  Enter a colon with the drive letter, followed by the backslash and 
  directory name, e.g. C:\BC5 The second parameter specifies the drive 
  where Borland programs are installed. Enter the drive letter followed 
  by a colon, e.g. D:
  Example: OHELPRPL C:\BC5 D:

/*************************  END OF FILE  ***************************/
