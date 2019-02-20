## Useful tips for Cmder - aliases and config sourcing ##

*Reloading (sourcing) Cmder config files (aliases, profile etc):*
Easy way this is to run the init.bat which is usually located in vendor folder which can be found in the Cmder root folder. Cmder creates windows cmd variable %CMDER_ROOT% which allows you to refernce to the cmder root. You should be able to relod the init script with this command:

%CMDER_ROOT%\vendor\init.bat

In case this would not work for some reason, you can call the script by using aboslute path. Let's say your Cmder is installed in:

C:\Cmder\

Than you can simply call:
 C:\Cmder\vendor\init.bat

It is also very useful to setup an alias for this, do it quickly. The user alias config is usually stored in this path:
%CMDER_ROOT%\config\user_aliases.cmd

You can open it in your favourite text editor and add this line:
init=%CMDER_ROOT%\Cmder\vendor\init.bat

Save the file and restart cmder, or call init.bat as shown above. Now whenever you type "init" in the Cmder command line. All the configs should be reloaded. Keep in mind that if you have two instances (tabs) with Cmder open, the config will be reloaded only in the window where you called the init from.

*More alias tips*
Alias file works similar to linux aliases in bash but the syntax is a bit different sometimes you don't need simple quotes ' but in some cases (especially when paths with spaces are resolved) you need to use double quotes. Like this:

```
help=cat "%CMDER_ROOT%\config\hotkeys-marek.txt"
gowork=cd "C:\Users\marek\Documents\Work"
```

Second alias moves me to my work folder. For the cd command to work properly you need to use double quotes. When you want to launch some file using let's say Adobe Acrobat which is installed in the Program Files. They you will need to use following alias:
```
mancdm="C:\Program Files (x86)\Adobe\Acrobat Reader DC\Reader\AcroRd32.exe" "C:
    \Users\marek\Documents\Documentation\manuals\field-manual.pdf"
```

