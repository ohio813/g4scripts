------------------
What is PassPass?
------------------
Meet PassPass (Bypass the Password), a nifty Grub4DOS batch script to disable/re-enable Windows logon password validation. Credit (as well as dis-credit) is to be equally shared between Wonko the Sane a.k.a. jaclaz and Holmes.Sherlock for the idea and coding respectively. We appreciate any success/failure report mentioning the following:

 - Windows version (e.g. XP, Vista, 7)
 - Service pack, if any
 - Architecture (e.g. 32-bit/64-bit)
 - msv1_0.dll version (e.g. 6.1.7600.16525) along with MD5 checksum, if possible

Technical details: The script tries to locate all existing Windows installations and corresponding Windows editions as well. Thereafter, it replaces the CMP instruction responsible for password verification with a 'benign' sequence of bytes. For reverting back the changes, the process is just the opposite. The whole idea is derived from WindowsGate and Astr0baby’s tutorial.


------------------
Usage:
------------------
 1. Install Grub4DOS. You may prefer using RMPrepUSB. Script tested with Grub4DOS v0.4.5c-2013-03-03.
 2. Download grubutils and copy WENV binary on the root of the boot media. Script tested with grubutils-2011-06-27.
 3. Copy PassPass, PassPass.bak and menu.lst on the root of the boot volume.
 4. Boot
 5. Ideally 'Autodetect' mode should be able to list out all existing Windows installation. For buggy BIOS-es, 
    try appropriate <Disk#> and <Partition#> to 'Forcedetect' Windows installations.
 6. Choose either 'Patch' or 'Unpatch' respectively for disabling/re-enabling password verification.
 7. Reboot and boot into target Windows.
 

------------------
Credits:
------------------
 - Wonko the sane – For ideas, code snippets, information. The script embeds his DLL version detection script
 - Ectomorph a.k.a. Damian Bakowski – For his 'unannounced' patch for 32-bit version of msv1_0.dll
 - Astr0baby – For his reversing tutorial
 - Steve Si – For including support for PassPass in his wonderful tool Easy2Boot


------------------
Project Details:
------------------
Download  : http://www.sherlock.reboot.pro/passpass-bypass-the-password/
Support   : http://reboot.pro/topic/18588-passpass-bypass-the-password/
Version   : Package contains PassPass v1.2 capable of patching both 32-bit and 64 bit versions of Windows XP, Vista, 7, 8 and 8.1
Revision  : PassPass v1.2 is based on Subversion revision 20
ChangeLog : https://code.google.com/p/g4scripts/source/list