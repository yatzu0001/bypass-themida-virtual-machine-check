# bypass-themida-virtual-machine-check




First you must edit the vm's (.vmx) file in the EXACTLY following lines
 - > svga.vramSize = 268435456 < -
- > monitor_control.restrict_backdoor = "TRUE" < -
- > monitor_control.disable_directexec = "TRUE" < - 
- > isoliation.tools.getPtrLocation.disable = "TRUE" < -
- > isoliation.tools.setPtrLocation.disable = "TRUE" < -
- > isoliation.tools.getVersion.disable = "TRUE" < -
 - > SMBIOS.reflectHost = "TRUE" < -
# then edit regedit keys of virtual machine with the following command in elevated command prompt:

reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Class\{4D36E968-E325-11CE-BFC1-08002BE10318}\0000" /v DriverDesk /t REG_SZ /d "ATI/NDIDIA SVGA II" /f





# mostly you are done now
