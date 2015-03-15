#How to use it

# Introduction #

Follow these steps to get the RSA Token on Windows Command Prompt


# RSA Token on Windows Command Prompt #

  1. Download the Source .ahk
  1. Open a Command Prompt
  1. Enter these commands:
```
C:\> rem Comment: XYZ is a folder that has the .ahk file you just downloaded and also the AutoHotkey.exe
C:\> cd XYZ
C:\XYZ>AutoHotkey.exe RSATokenAutomation.ahk

C:\XYZ>30958787
C:\> rem Comment: The above number is the passcode
C:\> rem Comment: The above script will only work if you don't do any mouse /keyboard movements
```

# RSA Token on Python #
  1. Make a .py script and use subprocess module.
  1. For example:
```
'''
Created on Nov 17, 2012

@author: ambarik
'''

import subprocess

def get_rsa_token():
    print "Getting RSA Token"
    return subprocess.Popen("./AutoHotkey.exe RSATokenAutomation.ahk", shell=True, stdout=subprocess.PIPE, cwd='/cygdrive/c/Barik/Softwares/AutoHotKey/RSA Token CLI Example').communicate()[0].strip()
```


# System Requirements #
  1. OS: Windows 7
  1. RSA SecureID 4.1.1
  1. RSA SecureID present at "C:\Program Files (x86)\RSA SecurID Software Token\SecurID.exe"
  1. AutoHotkey.exe from autohotkey.com
  1. Python 2.6 from www.python.org