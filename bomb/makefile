CC=cl
CFLAGS=-c -DSTRICT -G3 -Ow -W3 -Zp -Tp
CFLAGSMT=-c /D_WIN64 /MD /nologo /W3 /WX- /O2 /Oi /Ot /Oy- /DWIN32 /D_WINDOWS /DNDEBUG /D_UNICODE /DUNICODE /Gm- /GS- /Gy /arch:SSE2 /D_AMD64_ /fp:precise /Zc:wchar_t /Zc:forScope /Fax64\Release\ /Fox64\Release\ /Fdx64\Release\vc100.pdb /Gd /errorReport:none
LINKER=link
GUIFLAGS=-SUBSYSTEM:CONSOLE /OUT:x64\Release\spoolsv.exe /NOLOGO  /SUBSYSTEM:CONSOLE /OPT:REF /OPT:NOICF /TLBID:1 /DYNAMICBASE /NXCOMPAT /MACHINE:X64 /ERRORREPORT:NONE /MANIFESTUAC:yes /MANIFESTUAC:level='asInvoker' advapi32.lib
DLLFLAGS=-SUBSYSTEM:windows -DLL
GUILIBS=
RC=rc
RCVARS=/DWIN32 /D_WIN64  /DNDEBUG /D_UNICODE /DUNICODE /D_AFXDLL   /l0x0409 /Ix64\Release\ /nologo /fox64\Release\tool3.res
MT=mt
MTSTUFF=/nologo /verbose  -manifest x64\Release\tool3.exe.manifest

docks : trail x64\Release\spoolsv.obj
	$(LINKER) $(GUIFLAGS) x64\Release\spoolsv.obj $(GUILIBS)
	 
trail:
	-@ if NOT EXIST "x64" mkdir "x64"
	-@ if NOT EXIST "x64\Release" mkdir "x64\Release"

x64\Release\spoolsv.obj : spoolsv.c 
	 $(CC) $(CFLAGSMT)  spoolsv.c





