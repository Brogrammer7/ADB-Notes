# ADB-Notes
ADB device connection and basic commands info

To use adb commands on Windows, you might need to annotate adb as .\adb

Example: .\adb devices instead of adb devices


Configure Terminal in Android Studio settings:

file -> settings -> Terminal -> Application Setting -> shell path: c:\windows\system32\cmd.exe


**Important note** BOTH YOUR PC AND PHONE MUST BE ON SAME WIFI NETWORK

1. to connect FIRST pair using port # from 'Pair with Code' button:

2. .\adb pair 192.168.xx.xxx:xxxxx

3. enter 6 digit code

4. THEN use port # from top area (not Pair with Code section!):

5. .\adb connect 192.168.xx.xxx:xxxxx 


To fix a connection error (you may need to connect over USB wire or restart phone device):

.\adb kill-server 

.\adb start-server

.\adb tcpip 5555

.\adb pair then connect (follow above example)


Specify device to run command:

.\adb -s emulator-5554 + (command of your choice)

.\adb -s R5CT5302E2F

open deep link:

.\adb shell am start -d "rally://single_account/Checking" -a android.intent.action.VIEW

.\adb -s R5CT5302E2F shell am start -d "rally://single_account/Checking" -a android.intent.action.VIEW

