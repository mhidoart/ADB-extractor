D:
if not exist D:\phoneData mkdir D:\phoneData 
set /a target = (%RANDOM%*500/32768)+1
echo %target%
 if not exist D:\phoneData\%target% mkdir D:\phoneData\%target%

cd D:\phoneData\%target%
adb pull sdcard/DCIM
adb pull sdcard/WhatsApp
adb pull sdcard