*This article was originally published on my steemit blog here: [https://steemit.com/windows/@marek.samec/app-tips-for-windows-power-users](https://steemit.com/windows/@marek.samec/app-tips-for-windows-power-users) 
This is an updated version.*

If you like your Windows workstation or you are forced to use Windows by your employer, here are some apps that can boost your productivity and effectiveness. Most of these tools are free and open source or at least have some type of free version available. I have tested these apps under Windows 7 and Windows 10 (except for Double commander which I extensively tested only under Windows 10) and they worked without major issues. With an exception for Autohotkey, all of them also work without admin rights.

### Autohotkey
Or just AHK in short. This software makes Windows much more useful. It allows you to map and script your own hotkeys. For instance, this simple mapping will launch Cmder terminal when you press Ctrl + Alt + t

    ; Launch terminal Ctrl + Alt + t
    
    ^!t::
    
    Run, C:\Users\marekuser\Applicaitons\cmder\Cmder.exe

    Return

But you can do much more. This, for instance, launches Outlook 'New message' dialog and adds the content of your clipboard to the **To:** field:


    ^+!n::        
    Run, "C:\Program Files (x86)\Microsoft Office\Office14\OUTLOOK.EXE" /c ipm.note /m "%clipboard%


My favorite use for AHK is to map keyboard shortcuts to the documents that I open often or map a shortcut that synces my local folder with the corporate NAS server via WinSCP. If you are into scripting, you can even write some basic utilities within AutoHotkey. It is capable of creating simple graphical windows, dialogs, and popups. Advanced operations with the system and windows explorer can be done with Windows shell commands (but be careful here, they can mess things up if used wrongly). 

You can check the [documentation](https://www.autohotkey.com/docs/AutoHotkey.htm)  or visit the [forums](https://www.autohotkey.com/boards/)  to see some other interesting user scripts.
Installation of AHK requires admin rights but you don't need them for regular usage after installation. Loading new scripts into AHK also does not require admin rights but some commands and scripts might not work, especially if they modify the registry or some system variables.

### Cmder 

If you are used to GNU/Linux desktops you will most likely miss a good console in Windows. In that case, Cmder might come in handy. It gives you classic windows CMD shell upgraded with some goodies normally available in Linux. One of the main advantages is nice command history and command completion thanks to the integrated clink. There are some applications from windows git bash console which is also integrated to Cmder by default. You can use commands like git, vim editor and some Linux commands that have a bit clunky alternatives on windows cmd (ls, less, grep and so on). You can also define your own aliases and add other executables such as python, fzf (great command line fuzzy search) and so on. Cmder is a fork of ConEmu so you can add any other consoles that you like and launch them from within Cmder. I've tested it with putty, kitty, Cygwin, babun and all worked fine. Just keep in mind that the keyboard shortcuts of these consoles might collide with Cmder so you might need to do some tweaking here and there.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/akgt9x80wf25wnagpqbm.jpg)

### Chocolatey

If you miss Linux-like package management under Windows then Chocolatey is something you should consider. It has it's own quite wide repository of free tools but also proprietary software. For instance typing `choco install doublecmd` in your Windows cmd or PowerShell will install Double Commander application. Chocolatey teams up very well with Cmder. You can set up some useful aliases to speed up the Chocolatey usage even more. The only downside is that it's not as fast and smooth as Linux package managers you might be used to. My experience is that searching sometimes takes quite long a time and installing bigger applications is definitely slower than with apt-get or pacman.

But personally, I still prefer to stare a few seconds on the cmd than open up the web browser, find and download a setup file, get blocked by a corporate firewall, then finding some mirror that is not blocked, etc. Please be aware that some corporate firewalls might block Chocolatey or it's repositories as well. In that case, there is not much you can do 🥺. Also if you want to install all the software, you need to run Chocolatey from the elevated command prompt (with admin rights). Depending on the company policy, this might sometimes be an issue. It is nevertheless still possible to install Choco without admin rights (install guide is [here](https://chocolatey.org/docs/installation#non-administrative-install))  but then you will be able to install only apps that can run in portable mode or apps that do not require admin rights to run (such as Notepad++).

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/sxsmmymgt6y0w238c680.jpg)

### Total commander

I think most of you have already heard about this program. The main feature is the twin pane view and some basic commands you can use to interact with the files and move them from one pane to the other. Although this setup might look a bit archaic, when you learn the shortcuts you'll become a king of the file management. Some people use Windows only because there is no full-fledged Total Commander for Linux. Total Commander has integrated archiver, FTP client, great file comparing features and other tools. All this is very useful for power users who don't want to lose time by constantly clicking around in the windows explorer. You can fast edit text files by hitting F4, copy to the other pane by F5 or quickly create a new folder by F7. You can connect to the remote file system or FTP and very conveniently select and copy/upload files there. If you have never used any similar file manager before it might feel a bit uncomfortable but with practice, you can become very fast and effective. Total commander can be used for free but you have to pass an intro window where you have to click on the right number to continue. Alternatively, you can purchase the license at https://www.ghisler.com/.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/43lh7fl0eyzszhfmrmcy.jpg)

### Double commander
A very good free alternative to Total Commander. It does not have all the features but you might find it sufficient for your needs. The FTP client is a bit more intuitive in Total commander in my opinion but there are things I like better in doublecmd, especially how the settings are organized. Overall Doublecmd is still highly customizable and runs both under Linux and Windows so you can transfer your experience between the two systems.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/wj7yq9trhxsiedra5wcs.jpg)
*My customized doublecmd with different pane colors.*

### Vivaldi browser
This browser is built by the people that were behind Opera in its early days and it is very customizable. It is easily controlled by keyboard and unlike other browsers allows you to customize shortcuts, create custom search engines and other useful features. I wrote a separate article about it [here](https://steemit.com/vivaldi/@marek.samec/get-productive-with-vivaldi-browser)  so I won't go into too many details here.  If you want to save time, you can create custom searches to search in the web apps you use every day.  The theme, colors and browser layout can be adjusted to your liking as well. On the picture below you can see how I have tabs aligned vertically on the left. Although Vivaldi is based on the open source Chromium it looks nothing like Chrome (with exception of few dialog windows and extensions). This might be a downside if you are not a fan of Chromium-based browsers, but the good thing is that the vast majority of Google Chrome plugins work in Vivaldi.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/qyw3tb8ugd8ec7t94w9n.jpg)
*Vivaldi with a dark theme and vertical tabs*

That's it. I hope this article was helpful and will improve your experience while working under Windows. Do you have some other tips? Feel free to share them in the comments 👇.  



*Disclaimer: 
I have been a Windows user for more than 20 years and I still use it at work ( I have to :-) ). I am also an enthusiastic Linux user for almost 3 years now.*
