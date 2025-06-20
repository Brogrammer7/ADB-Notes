# ADB-Notes
ADB device connection and basic commands info

To use adb commands on Windows, you might need to annotate adb as .\adb

Example: .\adb devices instead of adb devices


Configure Terminal in Android Studio settings:

file -> settings -> Terminal -> Application Setting -> shell path: c:\windows\system32\cmd.exe


**Important note** BOTH YOUR PC AND PHONE MUST BE ON SAME WIFI NETWORK

To connect wirelessly via ADB if drop-down doesn't work:

1. Enable Wireless Debugging in Settings - Developer Options.
  
2. To connect, FIRST pair using port # from 'Pair with Code' button:

3. .\adb pair 192.168.xx.xxx:xxxxx (where xxxxx = port # from Pair with Code section)

4. input 6 digit code & hit enter

5. THEN get port # from top area (not Pair with Code section!):

6. .\adb connect 192.168.xx.xxx:xxxxx (where xxxxx = port # from top section)


To fix a connection error (you may need to connect over USB wire or restart phone device):

.\adb kill-server 

.\adb start-server

.\adb tcpip 5555

.\adb pair then connect (follow above example)


Specify device to run command:

.\adb -s emulator-5554 + (command of your choice)

.\adb -s (device id name)

open deep link:

.\adb shell am start -d "rally://single_account/Checking" -a android.intent.action.VIEW

.\adb -s (device id name) shell am start -d "rally://single_account/Checking" -a android.intent.action.VIEW

