![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vylznbda0cy1qssqskea.png)
Tiling window manager users often claim they bring superior productivity, are light on resources, and offer excellent customizability. But is it really true? Let's discuss this a bit and let's have a look at some tiling WMs for Linux. Although Linux is their main domain you can also find tiling scripts for Windows and even macOS.

## What is a tiling window manager?
First, do you actually know what is a tiling window manager? Most of you are probably familiar with stacking window managers which are used in Windows and macOS. It means that when you open a new window, it will appear on top of other windows. You can freely move it, resize it, minimize it, and so on. Tiling window managers take a different approach. The windows are automatically arranged in a predefined pattern. On top of that, the windows will be automatically moved and resized to match this pattern. The most common patterns are:

**Spiral:**
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/snogmbpzd5ov0hgmt2l0.png)

**Master window with a left or right stack of secondary windows:**
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/7il223vsm1srpujys3pk.png)

**Stripes**
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/f2g2vls6mpw39zbairv7.png)
**Centered master**
![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/rfw1f97t158a19uuwe0g.png)

**And many more...**


Your first thought might be that this can be quite limiting. In some cases, yes, but it also frees you from using the mouse to some extent. Most of these WMs also allow you to make some of the windows floating or draw them on top of others regardless of the active pattern. Often, you have to specify which windows will behave like this, but mostly this will be applied for dialog windows, popups, and so on. As you can see when you have too many windows open, some of them can become very small. To offset this, tiling WMs rely heavily on workspaces or tags that you can assign to the windows. You can then easily switch between workspaces and it can appear as easy as switching weapons in Quake 3 arena.

## But why?
That's a good question. If you'll watch some of the tiling window manager enthusiasts on YouTube (links are at the end of this article), you may notice that they use the terminal a lot and when they edit text or code they don't use fancy IDEs like Eclipse, vscode, Pycharm, etc. Instead, they use vim, emacs, and other applications that can run directly in the terminal.

Most of the tiling WM's were actually designed to be mainly used with terminal windows (or with terminal emulator windows to be more exact). These did not come from product designers thinking about simple user experience like Steve Jobs, but from programmers and sysadmins who spend a lot of time in the terminal, need to have multiple terminal windows open at the same time, etc. These people just want the system to get out of their way and let them do their job. Nice gui and buttons are not the priority here. Instead, the emphasis is put on usability, keyboard-centric design, and minimalism. But can tiling WMs really deliver on this promise?

## Terminate gui, switch to the terminal
Well, yes and no. Tiling WM can indeed speed up your work when you mostly use terminal apps. It is so easy to open a new terminal (usually just press Super + Enter). A super key can be (Win, Cmd, or another key which you can define). If your daily routine is connecting to remote servers, installing stuff, writing server scripts, you might not touch the mouse for hours.


![Alt Text](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/w5utoeupani412wz0a5l.png)
> This is a pretty old picture from the awesomewm home page. It illustrates its best use-case pretty well. Source: awesomewm.org

BUT. If you need to use many different gui apps it can get pretty messy. For instance, you have 4 web apps open in different browser tabs, you need to copy values from multiple excel/LibreOffice sheets paste them in your ticketing tool, then run few commands in the terminal, copy and send the results to your colleague via Slack, etc. you will find yourself juggling with the workspaces windows, tiling, untiling the windows, etc. That's simply because forced tiling can make some apps behave weird and you will need to add specific configurations to your WM to make them usable. In the end, you will spend time fighting with your environment and it will just make you slower.

Of course, some folks are not programmers or Linux/Unix admins and they still use tiling WMs. For instance, if you are a (data) scientist who prefers minimal statistical apps like R, you write your papers using LaTeX or Groff you don't need a fancy desktop environment like GNOME or KDE. You might prefer a minimal environment, where you can get stuff done. If you occasionally need to use more gui apps, you can still make it work if you have multiple monitors and you will create a fixed cockpit-like workspace: browser opens on a screen A, your terminals are on a screen B. The other less used apps are on a different workspace etc. But if you suddenly need to add some more stuff into the mix you will start to sweat.

## Minimized bloat, over-maximized configuration
Another important part is the configuration. None of the tiling WMs that I know comes with a settings app where you can just press buttons, select values, and configure your desktop environment. Instead, you edit a text configuration file. Examples are **i3**, **bspwm** or **xmonad**. Some WMs don't even have the config file and you have to directly edit the source code and recompile the WM after every change. A very good example is **dwm**. One can also find something in between like **awesomewm** where you basically edit Lua script code that generates parts of the WM gui. If you felt quite good until now, chances are that now you are much less optimistic about ever using something like this.

Do you dislike somewhat bloated environments like GNOME, KDE, or Cinnamon? Then you might just feel at home with let's say **awesomewm** or **bspwm**. But while using one of these you will realize just how much of the ordinary things DEs do for you. Wifi connection, sound management, tray icon, start menus, all these things are usually not part of the basic feature set of tiling WMs. It will be your task to find utilities to fill these gaps or use basic Linux services and GNU components and create your own simple gui. It's easier with some WMs' harder with others. For some users, it became something like a mantra: *"If you don't build your own desktop, you're not the troo 'nix haxxor..."*


## Conclusion
If you feel limited by the traditional stacking window managers you can give tiling WMs a try. My recommendation is to start with i3 as it offers quite many features out of the box and even gives you nice intro into how to set it up. Later you can try something more advanced. You can also use tiling WM alongside your DE and see how you'll like it. I use awesomwm and KDE Plasma. It actually works quite well, I just had to figure out how to make some things work together (integrate Kwallet, use Klipper for shared clipboard history, etc.). You can make the DEs work with GNOME, KDE, or XFCE apps and daemons running in the background.

Some links for further reading/watching:
Check [DistroTube](https://www.youtube.com/channel/UCVls1GmFKf6WlTraIb_IaJg), [Luke Smith](https://www.youtube.com/channel/UC2eYFnH61tmytImy1mTYvhA), [Brodie Robertson](https://www.youtube.com/user/OmegaDungeon), or Donald Feury for the start.
