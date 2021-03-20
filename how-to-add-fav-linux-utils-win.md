# How to add your favourite linux utilities to Windows command line

Ok, let's make this short. I am not in a mood for a long article today:

## Download the utilities 

**curl**
https://curl.haxx.se/windows/

**xmllint**
This is a bit harder, you have following options:
1. Copy xmllint and all the necessary libraries from your Cygwin install (if you have it).
2. Use chocolatey package manager and install xsltproc package. It contains xmlling, iconv, xmlcatalog. Simply type `choco install xltproc`

**GNU core utils (ls, grep, cat, tail,  mkdir and much more...)**
You can get theme here:
http://gnuwin32.sourceforge.net/packages/coreutils.htm



## How to install these

### Installing directly to your Windows cmd (no special advanced terminal like Cmder or ConsoleZ needed)
You can download these utilities to one folder for instance C:\utils\gnu-linux\ Just place all the *.exe files and all the related *.dll libraries to that folder.

Step 2 is adding this path to your System or User environmental variables for Windows. This way they will be auto added to your system %PATH% variable after Windows boot. Which is very similar to linux $PATH. Go to Start menu and type typing "envir" in the search box then "Edit the system envrionment variables" or "Edit environment variables for your account" if you want to make this change only for the current user. In the corporate environment you will most likely not be able to edit the variables for the whole system. But be careful! Do not delete anything default from the PATH, especially in case of the system variables. If the search does not work you can also open Control panel, go to "User accounts" and there click on the "Change my environmet varaiables" link on the left.Last option is to fire up the command line and run following command which will open the environment variables window directly:

```
C:\windows\system32\rundll32.exe sysdm.cpl,EditEnvironmentVariables
```


