---
title: Linux Desktops
---

The lower level is {{< iref "xorg" "Xorg" >}}

See also the section {{< iref "file_managers" "File Managers" >}},
{{< iref "xterminals" "X Terminals" >}},
{{< iref "#desktop_components" "Desktop components" >}}.

--------------

# Desktop environments {#desktop_environments}

A {{< wp "Desktop environment" >}} refers to a style of graphical user interface and also to a
common set of libraries ({{< wp "Widget library" >}}) used to build the desktop components.

Presently most desktop environment use either {{< wp "Qt_(framework)"  "QT" >}} or
{{< wp "GTK+" >}}, they include various
{{< iref "#desktop_components" "desktop components" >}}, mainly
a {{< iref "#window_manager" "window manager" >}}
and a {{< iref "#file_manager" "file-manager" >}}.

Some [window manager]((#window_manager "internal reference") are inseparable
from the desktop environment they use as _i3_, _fluxbox_, _awesome_
 and many light window manager. You will find an entry for them in the
{{< iref "#window_manager" "window manager section" >}}

You find a nice [comparison of memory footprints of  light linux desktops
](http://l3net.wordpress.com/lightweight-linux/)  in
[layer3 networking blog](http://l3net.wordpress.com/).

Wikipedia {{< wp "Comparison of X Window System desktop environments" >}}
gives also some information on the size of each-one.

## Main stream desktop environment

They are called _full desktop environment_
but we should call most of them _greedy_ as they eat 80% of the resources of you machines.
I don't use them so this list is brief.

-   {{< wp "KDE" >}} and {{< wp "KDE Software Compilation" >}}.
    [ArchLinux: KDE](https://wiki.archlinux.org/index.php/KDE)
-   {{< wp "GNOME" >}} there is the older Gnome2 and the newer Gnome3, look at
    {{< wp "GNOME"  "Wikipedia" >}} to learn about the differences and
    {{< wp "Controversy over GNOME 3" >}}.
    [ArchLinux: GNOME](https://wiki.archlinux.org/index.php/GNOME)
-   {{< wp "Unity" >}} is a shell interface for the GNOME desktop environment developed by
    Canonical Ltd for its Ubuntu operating system.
    [ArchLinux:Unity](https://wiki.archlinux.org/index.php/Unity)
-   {{< wp "MATE" >}} is a desktop environment forked from  GNOME 2.
    [ArchLinux: Mate](https://wiki.archlinux.org/index.php/MATE)
-   {{< wp "Cinnamon_(user_interface)"  "Cinnamon" >}}  is a fork of GNOME Shell based
    on the desktop metaphor, like GNOME 2. Cinnamon uses  as window manager _Muffin_,
    a fork of the GNOME 3 window manager _Mutter_.
    [ArchLinux: Cinnamon](https://wiki.archlinux.org/index.php/Cinnamon)

##  Xfce {#xfce}

[Xfce](http://en.wikipedia.org/wiki/Xfce "Wikipedia: Xfce") (GPL and LGPL) is a
desktop, which aims to be thinner and faster than gnome/kde, still
conforming to freedesktop platform. xfwm4 weight 6.5M resident,
xfce4-panel 8.8M, xfdesktop 8.5M, xftaskbar4 6.3M, xfce-mcs-manager
4.3M, xfce4-session 4.2M, and the file manager thunar 11M; of
course we cannot sum up these because there is shared memory, if
you add thunar on the top of a whole xfce session, you add only 5M
out of 10M because half of the resident size is truly shared (6.8
is sharable), a whole xfce session (without thunar) amount to 20M
on my computer. xfce4 is not so small than it aims to be.

-   [xfce Home](http://www.xfce.org/ "xfce.org Home") (GPL and LGPL)
-   [ArchWiki: Xfce](https://wiki.archlinux.org/index.php/Xfce)

## LXDE  {#lxde}

{{< wp "LXDE" >}} (GPL and LGPL) is a lightweight desktop environment for
Unix. It uses  the GTK+ toolkit. The components of lxde are not
strongly bound with a common library set as in KDE, Gnome or Xfce.
The standard component include the  window manager
{{< iref "#openbox" "Openbox" >}}, the session manager
{{< iref "#lxsession" "lxsession" >}}, the panel {{< iref "#lxpanel" "lxpanel"<}}
and the file manager {{< iref "file_managers#pcmanfm" "PCManFM" >}})
_but you are free to use an other one_.

-   [LXDE Home](https://lxde.github.io/)
-   [LXDE Wiki](http://wiki.lxde.org/en/Main_Page)
-   [LXDE - GitHub](https://github.com/lxde)
-   [ArchLinux: LXDE](https://wiki.archlinux.org/index.php/LXDE)
-   [LXDE on Debian](http://wiki.lxde.org/en/Debian)
-   [Gentoo: XDE](https://wiki.gentoo.org/wiki/LXDE)
-   [LXDE in Ubuntu](http://wiki.lxde.org/en/Ubuntu) is available on
    -   [Lubuntu](http://lubuntu.me) - Ubuntu with LXDE.
    -   [LXLE](http://lxle.net) - Lubuntu customized for aging computers.
    -   [WattOS](http://www.planetwatt.com/) \- Designed for older and low power
        computers. _site not available in July 2020_
    -   [Knoppix](http://knoppix.net/) - live CD with LXDE
-   [Lxde-Openbox Guide](http://lxlinux.com/index.html)has a lot
    information on configuration of all components of lxde.
-   <a name= "lxsession"></a>[lxsession](http://wiki.lxde.org/en/LXSession) is the
    standard session manager for LXDE, it has minimal footprints 1.7M resident/1.4M
    shared. But if you want to manage yourself the session you can dispense with it and
    use a simple launcher as _fbautostart_.
-   <a name= "lxpanel"></a>[LXPanel](https://wiki.lxde.org/en/LXPanel)
    is the standard panel of LXDE, it can generate a menu from _.desktop_ files. It can
    be configured from a GUI preferences dialog, and has theming support via custom
    gtkrc file.

# Window managers

See also the the
{{< iref "#desktop_environments" "Desktop environment" >}} and
{{< iref "#desktop_components" "Desktop Components Page" >}}

-   Wikipedia {{< wp "Comparison of X window managers" >}} gives the characteristics:
    Language, License, Type (stacking/dynamic/tiling), Configurable
    titlebar buttons, Graphical configuration, Hotkeys,	ICCCM/EWMH
    compliant, Panel for window switching, Tabbed windows,
    Themeable.<br />
    The light window managers are also compared with full environments
    in the {{< wp "Comparison of X Window System desktop environments" >}}.
-   [ArchWiki - Window manager
    ](https://wiki.archlinux.org/index.php/Window_manager)
-   [ArchLinux list of Window Managers
    ](https://wiki.archlinux.org/index.php/Window_Manager)
-   [ArchLinux Comparison of Tiling Window Managers
    ](https://wiki.archlinux.org/index.php/Comparison_of_Tiling_Window_Managers)
-   [Window Managers for X]((http://xwinman.org/),
    is an outdated comparaison of main window managers, with their characteristic. The
    [comparison page](http://xwinman.org/comparisons.php)
    compare the features and resource requirements. I also give some
    resident memory size on my amd64 on this page.
-   [Matchbox
    ](https://www.yoctoproject.org/tools-resources/projects/matchbox)
    is a base
    environment for the X Window System running on non-desktop embedded
    platforms. Matchbox is now part of the
    [Yocto Project](https://www.yoctoproject.org/) that provides tools
    to create custom Linux-based systems for embedded products.


-   {{< wp "Compiz" >}} is a {{< wp "Compositing window manager" >}} that can be used with gnome or KDE.
    - [Compiz Home](http://www.compiz.org/).
    - [Phoronix: The Cost Of Running Compiz](http://www.phoronix.com/scan.php?page=article&item=compiz_speed_test).
    -   [Gentoo Compiz Fusion HowTo](http://en.gentoo-wiki.com/wiki/Compiz-Fusion)
-   {{< wp "Mutter" >}} is a {{< wp "Compositing window manager" >}} and the standard window manager for Gnome.
    -   [Phoronix: Mutter Can Cause A Gaming/OpenGL Performance Hit Too
        ](http://www.phoronix.com/scan.php?page=article&item=mutter_composite_hit)

## EWMH {#ewmh}
The
[Extended Window Manager Hints (EWMH) specification
](http://standards.freedesktop.org/wm-spec/latest/)
is the freedesktop standard API to interact with a window manager.
This specification complete the
{{< wp "inter-Client_Communication_Conventions_Manual"  "Inter-Client Communication Conventions Manual (ICCCM)" >}},
which defines window manager interactions at a lower level.

The [wmctrl page](http://tripie.sweb.cz/utils/wmctrl/)
and the {{< wp "EWMH"  "Wikipedia EWMH page" >}} give some window managers that
implement EWMH _aewm, awsome, blackbox, bspwm, compiz, edwm,
enlightenment, evilwm, fluxbox, fvwm, i3, icewm, interfacewm, jwm,
kwin, matchbox, metacity,openbox, pekwm, penbox, sawfish, spectrwm,
waimea, wmfs, window maker, wmii, xmonad, xfce, xfwm_

Some window managers  do not implement
EWMH _ratpoison, ion, pwm, evilwm, flwm, windowlab, ctwm_. Of course
this incomplete list is subject to change with new releases.

The window managers that are EWMH compliant are also
{{< wp "inter-Client_Communication_Conventions_Manual"  "ICCCM" >}} compliant
as it is the base of EWMH. You can find on line the
[ICCCM specification](http://tronche.com/gui/x/icccm/).

See also the {{< iref "#wm_control" "WM Control" >}} subsection.


## Low resource tiling and dynamic Window Managers {#tiling_wm}

A tuttorial to desktop configuration with tiling wm:
[Home Sweet Home](http://blog.z3bra.org/2013/10/home-sweet-home.html)
with sections on the
[windows bars](http://blog.z3bra.org/2014/04/meeting-at-the-bar.html),
[popup notifications](http://blog.z3bra.org/2014/04/pop-it-up.html),
[colors settings](http://blog.z3bra.org/2015/06/vomiting-colors.html).

There is also a [Tutorial index
](https://www.reddit.com/r/unixporn/wiki/links/external).

-   [Awesome](http://awesome.naquadah.org/)
    _active project_,
    a framework dynamic window manager which follows Freedesktop
    standards, {{< iref "#ewmh" "EWMH compiliant" >}},
    and is extensible using Lua. It is packaged in Debian.
    -   [Alberto Pettarin: awesome is awesome!
        ](http://www.albertopettarin.it/blog/2015/07/07/awesome-is-awesome.html)
-   <a name=dwm"></a>[dwm](http://dwm.suckless.org/)
    is a minimalistic window manager. It manages windows in tiling,
    monocle -i.e. stacked_ and floating modes. It is part of the
    [suckless software](http://dwm.suckless.org/) and is packaged in
    Debian.

    There is also a derivative aimed to the console terminal
    {{< iref "console#dvtm" "dvtm" >}}.
-   {{< iref "#i3_wm" "i3" >}} has its own section.
-   {{< wp "larswm" >}} _last release 2004_ a dynamic, tiling window manager
    following _9wm_ model. It is _(yet)_ packaged in Debian.
-   [RatPoison](http://www.nongnu.org/ratpoison) (GPL)
    is a simple light window manager with nographics, no window
    corations, and no mouse/touchscreen/touchpad dependence.  All
    interaction with the window manager is done through keystrokes.
    <br/>
    The screen can be split into non-overlapping frames. All
    windows are kept maximized inside their frames.
        - {{< wp "Ratpoison"  "Wikipedia Ratpoison page" >}}
        - [RatPoison manual](http://www.nongnu.org/ratpoison/doc/)
        - [ArchLinux RatPoison tutorial](http://wiki.archlinux.org/index.php/Ratpoison)
        - [Gentoo Ratpoison HowTo](http://en.gentoo-wiki.com/wiki/Ratpoison)
-   [wmii](http://wmii.suckless.org/) is a dynamic window manager for X11,
    which is highly customizable via scripts and
    usable with keyboard and mouse. It supports conventional, tabbed and tiled
    window management with low memory usage. It is the predecessor of
    {{< iref "#i3_wm" "i3" >}}

## Low resource Stacking WM

-   [aewm](http://www.red-bean.com/~decklin/aewm/) (MIT License)
    _last release end 2007_, which is controlled entirely with the
    mouse. It is {{< iref "#ewmh" "EWMH compliant" >}} and is in Debian.
-   [aewm++](http://sapphire.sourceforge.net/) (MIT License)
    _active project packaged in Debian_
    based on aewm but  written in C++.
    -   aewm++ contains desktop utilities packaged in Debian as
        aewm++-goodies, an apllication bar, a panel, and a session
        manager.
        It is {{< iref "#ewmh" "EWMH compliant" >}}.
-   [evilwm](http://evilwm.sourceforge.net/) (Artistic licence)
    _active project_, A minimal keyboard driven window manager. It
    supports {{< iref "#ewmh" "EWMH" >}} and is packaged in
    Debian.  _last release 2011_
-   [Icewm](http://www.icewm.org/) (LGPL)
    a light {{< iref "#ewmh" "EWMH compliant" >}} wm,
    fully usable with keyboard, with a task bar, multiple workspaces
    and configuration tools.<br />
    It uses few libraries outside of standard X11, and its own library
    libice; so its real footprint is quite low: 6.2M resident/4.5M
    shared without desktop addons icewmtray 3M/2.3M, icewmbg 2.7M/2.2M
    _a background daemon is not mandatory_, icewm-session 1.7M/1.3M.
    -   [Gentoo IceWM HowTo](http://en.gentoo-wiki.com/wiki/IceWM)
-   [JWM (Joe's Window Manager)](http://www.joewing.net/programs/jwm/)
    (GPL) _actively maintened__ is a low resource (half the memory
    footprint of Fvwm95) Window manager using only Xlib and
    (optionally) the shape extension and libXpm. It is said to be
    one of the window managers with less dependencies, and smaller footprints.
    It supports {{< iref "#ewmh" "EWMH" >}}
    and is packaged in Debian.
-   [Oroborus](http://www.oroborus.org/) _minimal maintenance since
    2005, but with bugfix in 2010_ minimalistic window manager.
    It is packaged in Debian.
    -   Oroborus comes with three small utilities _KeyLaunch_,
        _DeskMenu_, and _DeskLaunch_ that are in separate debian packages.
-   [WindowMaker](http://www.windowmaker.org/ "windowmaker.org") (GPL)
    a tiny (1.3M rsz) and fully functional wm
        [Doc App Warehouse](http://www.bensinclair.com/dockapp/).

## i3 {#i3_wm}

[i3](http://i3wm.org/) (BSD Licence) is a tiling window manager
written in C. It is ewmh compliant. I3 has a dynamic switching to
floating, on an individual window base.

-   [i3 documentation](http://i3wm.org/docs/):
    [user guide](http://i3wm.org/docs/userguide.html),
    [External workspace bars such as i3bar or dzen2
    ](http://i3wm.org/docs/wsbar.html)
-   [Lukáš Zapletal’s i3 configuration
    ](http://i3wm.org/docs/user-contributed/lzap-config.html)
-   {{< wp "I3_(window_manager)"  "Wikipedia: I3" >}}
-   [GitHub mirror of i3](https://github.com/mgsnova/i3/)
-   [ArchLinux: I3](https://wiki.archlinux.org/index.php/I3)
-   _I3_ use [i3status](http://i3wm.org/i3status/manpage.html) to generate
     a status line for i3bar, dzen2 or xmobar.
-   [i3: IPC interface (interprocess communication)
    ](http://i3wm.org/docs/ipc.html)
-   [i3blocks](https://github.com/vivien/i3blocks)
    status line for the i3 window manager. It handles clicks, signals
    and language-agnostic user scripts.
    -   [i3blocks wiki](https://github.com/vivien/i3blocks/wiki)
        give example of _i3blocks_ scripts, and explain how to write
        your own.
-   [i3 doc](https://github.com/i3/i3/tree/next/docs) contain tools,
    the userguide, the refcard &#x2026;

The window manager alone uses 5.9M/4.8M, the i3bar 5M/4.2M, i3status
1.6M/1.3M.

We can use [i3blocks](https://github.com/vivien/i3blocks)
to replace _i3status_  With the standard configuration which
mimic i3status _i3blocks_ has a memory footprint of 0.7M/0.5M to
which are temporarily added the called programs to update status.

### i3 tools and scripts
-   [i3status](http://i3wm.org/i3status/manpage.html) (BSD Licence)
    is a small program for generating a status bar for
    i3bar, dzen2, xmobar or similar programs.
-   [i3pystatus](https://github.com/enkore/i3pystatus)
    is a  collection of python 3 scripts for status output
    compatible to i3status / i3bar.
    -   [i3pystatus documentation
        ](http://i3pystatus.readthedocs.io/en/latest/)
-   {{< iref "#j4status" "j4status" >}} below is an alternative
    to _i3-status_;
-   [GitHub: i3-py](https://github.com/ziberna/i3-py)
    contains python tools for i3. No new commit since 2012 there are many forks, but
    nobody seems to maintain the repository.<br /> The script _winmenu.py_ launches
    {{< iref "#dmenu" "dmenu" >}} (with vertical patch) with a list of clients, sorted
    after workspaces. Selecting a client jumps to that window.
-   [GitHub: quickswitch-for-i3
    ](https://github.com/proxypoke/quickswitch-for-i3)
    ( [WFPT Licence](http://sam.zoy.org/wtfpl/COPYING))
    is a python script using _i3-py_ that
    allows you to quickly switch to and locate windows on all your
    workspaces, using an interactive
    {{< iref "#dmenu" "dmenu" >}} prompt.
    A more recent fork is [Oliver Uvman - quickswitch-for-i3
    ](https://github.com/OliverUv/quickswitch-for-i3)
-   [GitHub: i3-wm-scripts](https://github.com/MicahChambers/i3-wm-scripts)
    is a collection of python scripts that contains:
    -   _nextmatch.py_ to jump to a window by matching a title regex.
    -   _nextfind.py_ to jump to a window choosen from a list.
    -   _mark_ to mark a window in a target list, _goto_ to jump to a
        window chhosen from the target list; _unmark_ to delete from
        the list.
-   [GitHub: i3-emacs](https://github.com/vava/i3-emacs) is an emacs
    package for i3-emacs integration.
-   [j4-make-config](https://github.com/okraits/j4-make-config)
    is a theme switcher and config generator for i3.

## Openbox {#openbox}

[Openbox](http://icculus.org/openbox/) is a window-manager with root menu, dock, no
taskbar (use fspanel, fbpanel, pypanel), a configuration management tool named
[obconf](http://icculus.org/openbox/obconf/ "icculus.org obconf").
Openbox is the standard window manager of {{< iref "#lxde" "Lxde" >}}
It can be used with many {{< iref "#file_managers" "file managers" >}}
most often with {{< iref "#pcmanfm" "PCManFM" >}}.

OpenBox use 10M resident memory including 5.5M shared.

-   [LXDE Openbox page](http://wiki.lxde.org/en/Openbox)
-   Gentoo
    [HOWTO Openbox](http://en.gentoo-wiki.com/wiki/Openbox).
-   [An Openbox Guide](http://urukrama.wordpress.com/openbox-guide/) and
    [Openbox Faq](http://urukrama.wordpress.com/openbox-faq/) in
    [Urukrama Web Log](http://urukrama.wordpress.com/)
-   man pages: {{< man "openbox(1)" >}}, {{< man "openbox-session(1)" >}}

## Fluxbox

[fluxbox](http://fluxbox.org/) (MIT license) is a small (5.8M resident
4.4M shared) fast and highly configurable window manager, with root
menu, dock (named slit here!), taskbar including the systray, tabbed
windows. The configuration management is integrated, there is also a
powerfull menu generating utility fluxbox-generate\_menu. Fluxbox is a
fork of [Blackbox](http://blackboxwm.sf.net/) and share with it some
[tools](http://bbtools.sourceforge.net/).

Fluxbox doesn't
depends on a specific toolkit and does not use any windowing toolkit
(no gtk/Qt binding) but can be used with any Freedesktop compliant
desktop; as the main program contain everything needed for a window
manager, you have not to use any add-on like systray or panel, it
makes fluxbox one of the lighter window manager. If you need to
compare with openbox you have to add the panel, and may be the systray
if the chosen panel does not include one.

-   The configuration and use
    of fluxbox is described in the _old_
    [Fluxbox Documentation
    ](http://fluxbox.sourceforge.net/docbook/en/html/book1.html)
    and now in the fluxbox wiki.
-   In the[fluxbox wiki](http://fluxbox-wiki.org/) you can find a
    [FAQ](http://fluxbox-wiki.org/index.php?title=FAQ), and a
    [list of HowTos
    ](http://fluxbox-wiki.org/index.php?title=Category:English_howtos)
    in the wiki.
-   In the wiki you find documentation about the fluxbox
    [configurations  files
    ](http://fluxbox-wiki.org/index.php?title=Category:Configuration_howtos)
    :
    -   [init file
        ](http://fluxbox-wiki.org/index.php?title=Editing_the_init_file),
    -   [apps file
        ](http://fluxbox-wiki.org/index.php?title=Editing_the_apps_file),
    -   [Keys File
        ](http://fluxbox-wiki.org/index.php?title=Keyboard_shortcuts)
        and [Key Modes
        ](http://fluxbox-wiki.org/index.php?title=Keymodes),
    -   [Menu file
        ](http://fluxbox-wiki.org/index.php?title=Editing_the_menu),
    -   [Window Menu
        ](http://fluxbox-wiki.org/index.php?title=Editing_the_windowmenu),
    -   [Startup file
        ](http://fluxbox-wiki.org/index.php?title=Editing_the_startup_file).
    -   [Keyboard shortcuts
        ](http://fluxbox-wiki.org/index.php?title=Keyboard_shortcuts)
        including [keychains
        ](http://fluxbox-wiki.org/index.php?title=Keyboard_shortcuts#Keychains),

-   [Gentoo: Fluxbox Configuration HOWTO
    ](http://www.gentoo.org/doc/en/fluxbox-config.xml)
-   [Ubuntu community: Fluxbox
    ](https://help.ubuntu.com/community/Fluxbox)
-   [Debian Wiki: Fluxbox](http://wiki.debian.org/FluxBox).
-   [Archwiki: Fluxbox](https://wiki.archlinux.org/index.php/Fluxbox) and
    [ArchWiki: Fluxbox Style Guide
    ](https://wiki.archlinux.org/index.php/Fluxbox_Style_Guide).
    fluxbox also supports [Key modes
    ](http://fluxbox-wiki.org/index.php?title=Keymodes)
-   [Akira's keyfile](http://darkshed.net/files/rcs/fluxbox/keys.html)
    date from 2005 but is still a very complete example.
-   Example of styles:
    [tenr fluxbox style](http://tenr.de/styles/) and
    [tenr Exemple of configuration](http://tenr.de/snippets/),
    [tenr HowTo style fluxbox
    ](http://tenr.de/howto/style_fluxbox/style_fluxbox.html)
-   The development tree is in [git.fluxbox](http://git.fluxbox.org/)
    There are instructions to
    [build fluxbox from source](http://fluxbox-wiki.org/index.php?title=Build_fluxbox_from_source).
-   [fluxbox-xdg-menu](http://code.google.com/p/fluxbox-xdg-menu/) is a small python script using
    [python-xdg](http://freedesktop.org/wiki/Software/pyxdg)
    to create a menu for fluxbox using freedesktop.org standards.
-   [fbxdgmenu](pyhttps://bitbucket.org/confluence/fluxbox-tools) is a
    fork of *fluxbox-xdg-menu*, it is a simpler program that only deal
    with menu not the background.
-   You can complete your fluxbox desktops with some other light
    components referenced in the
    {{< iref "#desktop_components" "Desktop components sections" >}}



### Fluxbox configuration

-   local man pages:
    [fluxbox(1)](http://localhost/man/1+fluxbox),
    [fbrun(1)](//man2html.php?1+fbrun),
    [fbsetbg(1)](//man2html.php?1+fbsetbg),
    [fluxstyle(1)](http://localhost/man/1+fluxbox),
    [startfluxbox(1)](/man2/startfluxbox)
-   The config is in `~/.fluxbox/init`
-   For Fluxbox I use the development version as advised on the
    wiki and the FAQ, since the stable version is old and no longer maintained.
-   [Fluxbox: Editing the menu
   ](http://fluxbox-wiki.org/index.php/Editing_the_menu) to generate a new menu:

        fluxbox-generate_menu -h

-   there is (was?) a the script fluxbox-generate-menu is in /usr/share/doc/fluxbox/fluxbox-generate_menu.gz
-   The user menu is in `~/.fluxbox/usermenu`
-   fluxbox menu editors:
   [fluxmenu](http://sourceforge.net/projects/fluxmenu.berlios/),
   (Fluxbox Menu Editor (fme)](https://github.com/rdehouss/fme) (2009)
   [marchfluxmenu (python)](http://code.google.com/p/marchfluxmenu/) (2007)
   use desktop files found in /usr/share/applications/.
-   On Debian a  debian menu is generated by
    `/etc/menu-methods/fluxbox`,
    it lies in `/etc/X11/fluxbox/` for system and `~/.fluxbox`
     when update-menu is launched by a non-root user. There are 4 files
    `menudefs.hook` the generated menu, `system.fluxbox-menu` the system
    menu, `fluxbox-menu` the concatenation of the two previous, and `menu`
    (prototype named `/etc/X11/fluxbox/fluxbox.menu-user`) the top level
    menu that will include others.
-   I also include a first file named usermenu for the customization.
-   The __fluxbox menu__ ''(right mouse)'' allow to configure the slit.
-   [ubuntuforum:  HOWTO: get a Fluxbox menu (and customization)
    ](http://ubuntuforums.org/showthread.php?t=371144)
-   the apps file allow to customize applications and
    [to tab windows together](http://www.fluxbox.org/features/).
-   fbsetbg relies on chbg,  display, Esetroot, feh,  qiv, hsetroot,
    icewmbg,  wmsetbg, xli xsetbg, xsri,
-   fbdesk needs icons the
    [collection of gentoo bubble icons](http://bubbleicons.tuxfamily.org/)
    is appropiate.



## icewm shortcuts
These are the most common keyboard shortcuts used in icewm to make your life easier:

- ctrl+esc opens the 'start menu'
- alt+f11 (word key) full screens any active window/application
- alt+f10 maximizes active window/application
- alt+f9 minimizes active window/application
- alt+f4 closes active window/application
- ctrl+alt+h hides the taskbar
- ctrl+alt+f1 from inside icewm brings you to console
- ctrl+alt+f2 brings you back to icewm desktop
- ctrl+alt+backspace kills X11 and brings you back to console
- alt+f1 - f3 in console to switch between 3 virtual consoles
- type 'reboot' in console to properly shut down the system, then pull the battery.

# Wayland compositors {#wayland_compositors}

See also the {{< iref "xorg#wayland" "Wayland Section" >}},
{{< iref "xterminals#wayland_terminals" "Wayland Terminals" >}}.

-   [Enlightenment](https://en.wikipedia.org/wiki/Enlightenment_(software)) (BSD
    License) is a compositing window manager for Xorg or a  since version 20 a Wayland
    compositor.
    -   [Enlightenment Home](https://www.enlightenment.org/)

## Wayland destop components
-   [imv](https://github.com/eXeC64/imv) is an image viewer for X11/Wayland.


# Desktop components {#desktop_components}
## Color Themes {#color_themes}

See also {{< iref "emacs#emacs_themes" "Emacs Themes" >}}.
-   [base16](https://github.com/chriskempson/base16)
    by Chris Kempson is the improvement of
    [tomorrow-theme](https://github.com/chriskempson/tomorrow-theme)
    it is very actively maintained
    It has color schemes for:
    _vim_, _shell_ (_bash_, _zsh_), _Xressources_, _XFCE4 Terminal_, _gimp_,
    _mate terminal_, _gnome terminal_, _emacs_, _zathura_ and _mac os_ apps.
-   [nord](https://github.com/arcticicestudio/nord) is an arctic, north-bluish color
    palette.
    -   [Nord Home](https://www.nordtheme.com)
    -   [nord vim](https://github.com/arcticicestudio/nord-vim)
    -   [nord tmux](https://github.com/arcticicestudio/nord-tmux)
-   [Solarized](http://ethanschoonover.com/solarized)
    is a sixteen color palette for vim, Xresources, emacs,  mutt,
    GIMP Palette; and some Mac OS apps. It is also
    [ported to gnome-terminal
    ](https://github.com/Anthony25/gnome-terminal-colors-solarized)
    which can easily be also adapted to roxterm.
-   [Smyck](https://github.com/hukl/Smyck-Color-Scheme),
    [Smyck Home](http://color.smyck.org/)
    is no longer updated since 2012, but has many forks.
    The ariejan fork has a [color scheme for roxterm
    ](https://github.com/ariejan/Smyck-Color-Scheme/tree/roxterm)
-   [Zenburn](http://sysphere.org/~anrxc/j/articles/zenburn/index.html)
    by [anrxc](http://sysphere.org/~anrxc/)
    has scheme for [awsome](http://awesome.naquadah.org/wiki/Zenburn_Theme),
    console, _Gajim_, _pidgin_, _emacs_, X apps thru
    _.Xdefaults _, [roxterm theme
    ](http://git.sysphere.org/dotfiles/tree/config/roxtnerm.sourceforge.net/Colours/Zenburn).

-   There are many web applications to help to configure color themes
    [256 colors - cheat sheet](https://jonasjacek.github.io/colors/),
    [terminal sexy](http://terminal.sexy/),
    [4bit Terminal Color Scheme Designer
    ](http://ciembor.github.io/4bit/),
    [colorschemedesigner](http://colorschemedesigner.com/csd-3.5/),
    [The 28 best tools for choosing a colour scheme (2014)
    ](http://www.creativebloq.com/colour/tools-colour-schemes-12121430).



-   For bash you can look at [ArchLinux: Color Bash Prompt
    ](https://wiki.archlinux.org/index.php/Color_Bash_Prompt)

## Panels {#panels}

Most window managers provide their own panel, only some small/micro manager use an external one.

-   _aewm++-fspanel_ (MIT) is a minimal panel developped with aewm++, but it
    does not depend on iT. It is in the debian package aewm++-goodies.
-   [fbpanel](http://fbpanel.sourceforge.net/) (GPL)
    FBPanel is a spinoff of the fspanel written -n c/GTK+.
    It provides a taskbar (list of all opened windows), pager, desktop switcher,
    launchbar, clock, and more through plugins is EWMH/NETWM
    compliant. _available in Debian_
    -   [fbpanel configuration](http://fbpanel.sourceforge.net/docs.html)
-   _fspanel_ (GPL)
    works with EWMH compliant WMs. _available in Debian_
-   _hpanel_ is a fork of _fspane_ to better handle maximized windows.
    _available in Debian_
-   [ltpanel](http://ltpanel.sourceforge.net/) (GPL)
    is a lightweight panel, looking similar to the gnome tasklist
    applet. It uses only xlib and has a very light memory footprint.
    It is based on Peter Zelzny's _fspanel_ and is available in Debian.
-   [LXPanel](http://lxde.org) is the  GTK+2 desktop panel for lxde, it
    has minimal gtk2 dependencies.
-   [pypanel](http://pypanel.sourceforge.net/) (GPLv2)
    is a lightweight panel/taskbar written in Python and C
    it works with EWMH compliant WMs (Openbox, PekWM, FVWM, etc.)
    -   [ArchWiki: pypanel](https://wiki.archlinux.org/index.php/PyPanel)
-   [tint2](http://code.google.com/p/tint2/)  (GPLv2)
    is a panel (made for openbox3 but without lxde dependencies)
    with taskbar,
    systray, clock and battery status and  window manager's menu.
    The mem footprints of tint2 is 6.7M resident / 5.2 shared<br />
    -   [tintwizard](http://code.google.com/p/tintwizard/) is a theme
        switcher for tint2.
    -   [ArchWiki: tint2](https://wiki.archlinux.org/index.php/Tint2)

## Menu system
### menus from shell
-   [qmenu](https://github.com/teopost/qmenu/)
    Features include options to format the menu, bindings to function
    keys, possibility to include submenus, show help messages and
    launch shell sessions.  package in Debian.
-   _9menu_ from plan9, [9menu Debian package
    ](https://packages.debian.org/testing/9menu)
-   _ratmenu_ forked from 9menu for ratpoison wm
    [ratmenu Debian package
    ](https://packages.debian.org/testing/ratmenu)
-   [Zrajm’s programs](http://zrajm.org/programs/) provide _ratmen_ a
    _ratmenu_ alternative, and _termmen_ a zsh menu.

### dmenu {#dmenu}
[dmenu](http://tools.suckless.org/dmenu/)
is a dynamic menu for X, originally designed for dwm. part of
the suckless-tools package in Debian.
-   [ArchWiki: dmenu](https://wiki.archlinux.org/index.php/dmenu),
-   [Archlinux dmnenu hacking thread
    ](https://bbs.archlinux.org/viewtopic.php?id=80145),
-   [jukil/dmenu-scripts-collection
    ](https://github.com/jukil/dmenu-scripts-collection)
    collected from the hacking thread _until 2014, newer scripts are not here!_.
-   [tlvince/dmenu-tools](https://github.com/tlvince/dmenu-tools).
    A collection of scripts in the _dmenu_tools_ AUR package:
    dmenu_edit, dmenu_menu, dmenu_mpc, dmenu_netctl, dmenu_raise, dmenu_raise_or_run,
    dmenu_run_recent.

### dmenu alternatives
-   [bemenu](https://github.com/Cloudef/bemenu) (GPLv3 and LGPLv3)
    is an dynamic menu library and client program inspired by dmenu.
    -   [bemenu API documentation](http://cloudef.pw/bemenu/).
-   [dmenu-pango-imlib](https://github.com/Cloudef/dmenu-pango-imlib)
    is a dmenu fork with pango and imlib support.
-   {{< iref "#lemonbar" "lemonbar" >}}
    in the status bar section.
-   [pdmenu](https://joeyh.name/code/pdmenu/) full screen console
    menuing system for Unix.
-   The [rliang repository](https://github.com/rliang)
    offer many derivatives of dmenu:
    -   [rliang/gdmenu · GitHub](https://github.com/rliang/gdmenu)
        a GTK+ dmenu clone.
    -   [rliang/cdmenu · GitHub](https://github.com/rliang/cdmenu)
        a Curses/console dmenu clone.
    -   [rliang/cpbar · GitHub](https://github.com/rliang/cpbar)
        a XCB-based panel for displaying textual information from
        STDIN using Cairo and Pango markup.
    -   [rliang/sdmenu · GitHub](https://github.com/rliang/sdmenu)
        a shell dmenu.
-   <a name="rofi"></a>[Rofi](https://davedavenport.github.io/rofi/) (MIT License)
    A popup window switcher requiring only xlib and pango.
    Rofi can act as a drop-in dmenu replacement and provides
    extra features, like a run-dialog, ssh-launcher, ....
    Rofi is written by Dave Davenport alias _Qball_ it is in Debian.
    -    [GitHub - DaveDavenport/rofi
        ](https://github.com/DaveDavenport/rofi)
    -    [Rofi - manpage](https://github.com/DaveDavenport/rofi/blob/master/doc/rofi.1.markdown),
    -    [Rofi wiki](https://github.com/DaveDavenport/rofi/wiki),
    -    [reddit - Qball tools forum](https://reddit.com/r/qtools/)
-   [slmenu](https://bitbucket.org/rafaelgg/slmenu/src) (MIT License)
    a dmenu clone for the console.<br />
    [slmenu, and some seriously wicked console wizardry
    ](http://inconsolation.wordpress.com/2013/03/16/bonus-slmenu-and-some-seriously-wicked-console-wizardry/)
    in [incosolation blog](http://inconsolation.wordpress.com).
-   {{< iref "#yabar" "yabar" >}} in the status bar section.

### Dzen {#dzen}
[Dzen](https://github.com/robm/dzen)
is a notification and menuing program for X11 rhat requires only X11.
It is designed to be
scriptable in any language and integrate well with light window managers.
A _dzen_ daemon takes only 1.5M res/1.1M shr.

-   The [Dzen Wiki
    ](https://github.com/robm/dzen/wiki) gives
    many examples of using _dzen_ as system monitor, with simple
    scripts.
-   [ArchLinux: dzen](https://wiki.archlinux.org/index.php/Dzen)
-   You can [pipe the output of conky
    ](https://wiki.archlinux.org/index.php/Dzen#Dzen_.26_Conky) to dzen.
-   Or [pipe the output of i3status
    ](http://i3.zekjur.net/i3status/).
-   [dzen-tools](https://github.com/dgvncsz0f/dzen-tools)
    by Diego Souza has
    _systat2dzen_, a python script that gives hostname, date/time, sys statistics,
    meminfo, iostat, load ifo, disk status, battery status, check
    local or imap mailboxes, ethernet and wireless status
-   [Creating an App. Launcher with Dzen2 and bash
    ](https://bbs.archlinux.org/viewtopic.php?id=45364)

### Root menu
Root menus are parts of most floating window managers, but there are
some stand alone:

-   [deskmenu (debian package)
    ](https://packages.debian.org/jessie/deskmenu).

### Freedesktop (xdg) menus {#xdg_menus}

They can be a root menu or a popup using one of the previous bars.
The python programs use
[PyXDG
](https://pyxdg.readthedocs.org/en/latest/_modules/xdg/Menu.html).

-   The Faq.i3wm forum [How can I use autostart .desktop files in i3?
    ](https://faq.i3wm.org/question/2155/how-can-i-use-autostart-desktop-files-in-i3/)
    teach how to use dex to test your autostart files.
-   [dmenu_launch
    ](https://github.com/Wintervenom/Scripts/blob/master/file/launch/dmenu-launch)
    by Scott Garrett (Wintervenom) in
    [GitHub: Wintervenom/Scripts](https://github.com/Wintervenom/Scripts).
-   [fluxbox-xdg-menu](http://code.google.com/p/fluxbox-xdg-menu/) (GPL)
    is a python based menu generator used to create a menu for fluxbox
    using freedesktop.org standards.
-   [Gmrun](https://sourceforge.net/projects/gmrun/)
    (Gnome Completion-Run) is an lightweight application launcher,
    with bash-like TAB completion, thet propose all the xdg desktop programs.
    -   [ArchWiki: Gmrun](https://wiki.archlinux.org/index.php/Gmrun)
-   Thomas Bellembois [i3-start-menu
    ](http://perso.ens-lyon.fr/thomas.bellembois/doku.php?id%3Di3_start_menu)
-   [j4-dmenu-desktop](https://github.com/enkore/j4-dmenu-desktop)
    it is an alternative (a lot quicker) for  i3-dmenu-desktop.
    _j4-dmenu-desktop_ doesn't require i3wm and work on any desktop
    environment.
-   [MenuMaker](http://menumaker.sourceforge.net/)
    is a python menu generation utility for: Blackbox, Deskmenu,
    FluxBox, IceWM, OpenBox, Pekwm, WindowMaker ,XFce4 it can use both
    of Freedesktop.org's .desktop files and Debian application
    entries. _last release 2005, dev tree from 2007_
-   [morc_menu
    ](https://github.com/Boruch-Baum/morc_menu/)
    is an categorized desktop application menu, independent of any window manager.
    it is an alternative for  i3-dmenu-desktop and [j4-dmenu-desktop
    ](https://github.com/enkore/j4-dmenu-desktop)
-   [uxdgmenu](https://github.com/ju1ius/uxdgmenu) (python) generates
    desktop menus for window managers, it supports currently
    Fluxbox, Openbox, Awesome, Blackbox, WindowMaker, FVWM2, IceWM,
    Ion3, PekWM, TWM _2013_
-   [ArchLinux xdg-menu](https://wiki.archlinux.org/index.php/Xdg-menu)
    generates menus for twm, ion3, WindowMaker, fvwm2, icewm,
    blackbox, fluxbox, openbox, awesome.
-   [xdgmenu](https://github.com/crichon/xdgmenu)
    is a python/ncurses application to launch a xdg menu.
-   [xdmenug
    ](https://raw.githubusercontent.com/sagotsky/.dotfiles/master/scripts/xdmenug.py)
    in [sagotsky dotfiles](https://github.com/sagotsky/.dotfiles)
    referenced in [dmenu toys](http://sagotsky.github.io/2013/10/11/dmenu-toys.html)
-   [GitHub - xdgmenumaker
    ](https://github.com/gapan/xdgmenumaker/) (GPL)
    is a command line tool, written in python (2 or 3), that generates
    application menus using xdg information, by scanning *.desktop
    files. It can generate menus for Fluxbox, IceWM, jwm, pekwm,
    Window Maker.

## Status Line {#status_line}
Most window manager have their own status bar and a status generation
programs or scripts, like _i3bar_ with _i3status_ or _i3blocks_.
But some alternative status are window manager independant.

-   <a name="j4status"></a>[j4status](http://j4status.j4tools.org/)
    (GPL) is an alternative
    to _i3-status_ but it is available on any tiling wm.
    It provides a status line using several plugins
    to retrieve system information.
    -   [j4status-plugins
        ](https://j4status.j4tools.org/j4status-plugins/)
        add plugins for _alsa_, _mpris_, filesystem, cpu and memory
        usage, backlight percentage, i3 focus, _networkmanager_, and
        an inotify plugein to _j4status_.
-   <a name="lemonbar"></a>[lemonbar](https://github.com/LemonBoy/bar)
    is a lightweight bar based on XCB. It provides
    foreground/background color switching along with text alignment
    and colored under/overlining of text, full utf8 support and
    reduced memory footprint.
-   [xmobar](http://projects.haskell.org/xmobar/)
    written in haskell,  is a lightweight, text-based, status.
    It was originally designed to work with xmonad,
    but it's actually usable with any window-manager. It is in Debian.
    It can be used for _conky_ or _i3status_ output.
    -   [ArchWiki xmobar](https://wiki.archlinux.org/index.php/Xmobar)
-   <a name="yabar"></a>[Yabar](https://github.com/geommer/yabar)
    (MIT License)
    is a lightweight status bar for X window managers.
    _Yabar_ is in debian.


## Launchers  {#launch_bars}
Launchers are also named _taskbar_, _launchbar_, _dock_ ....

-   [i3status](http://i3.zekjur.net/i3status/)
-   _aewm++-appbar_ (MIT) is a minimal launchbar developped with aewm++, but it
    does not depend on iT. It is in the debian package aewm++-goodies.
-   [tabble](http://www.rillion.net/tabble/) (GPL) is a small
    rectangular widget written  in C/GTK2  which presents your
    programs in tabs for easy launch. It can also be launched with
    sudo to give an easy root access to some programs.The last release
    is 2012. It is in  debian.
-   [wbar](http://code.google.com/p/wbar/source/browse/trunk/README)
    is a C++/gtk launch bar. It was initially developed for Fluxbox,
    then tested on WindowMaker, Xfce, GNOME, etc. It is in Debian
    -   _wbar-config_ is the recommended tool to customize Wbar. In
        debian it is in a separate package.
-   [lxlauncher](http://wiki.lxde.org/en/LXLauncher) is a
    launcher for application programs developed for the 7"-10.2"
    screens (netbooks) it follows freedesktop.org
    specs.
-   [Cairo-Dock](http://www.glx-dock.org/)
    is a highly customizable dock (_not light_) written in C. It is in
    debian. It can be controlled from a terminal or another
    application through the DBus interface.
    Features can be added by plug-ins or applets.
    -   [Cairo-Dock - ArchWiki](https://wiki.archlinux.org/index.php/Cairo-Dock).
-   [Launchpad: Avant Window Navigator (Awn)
    ](https://launchpad.net/awn)
    is a dock-like bar which sits at the bottom of the screen. It is
    for composite window managers and no longer in Debian.
    -   [Avant Window Navigator - ArchWiki
        ](https://wiki.archlinux.org/index.php/Avant_Window_Navigator)

## Pin boards
Pin boards allow to create icons on your desktop and to associate
some command or action to the icon.

Some desktop include a built in pin board as _Gnome_ through its file
manager _Nautilus_.

_Pcmanfm _also has an option to manage the desktop, and you can then
use desktop shortcuts.

You can choose to not have a pinboard on your desktop. A pinboard is easily
hidden by floating windows, and is a non-sense with tiling wm that use
all the screen but to use a menu system or a
{{< iref "#launch_bars" "Launch Bar" >}}.

-   [fbdesk](http://fluxbox.sourceforge.net/fbdesk/) (3.8M) aimed at
    FluxBox/BlackBox, it is in debian.
-   [idesk](http://idesk.sourceforge.net) (9.2M) _last release 2005_.
    If you want to fatten a thin window manager it's the way.
-   Desklaunch from the
    [Oroborus Window Manager](http://www.oroborus.org/), but which can
    be used with an other minimal wm.
    DeskLaunch is a small utility for creating desktop icons using pixmaps.
    It is, as a
    [separate package in debian](https://packages.debian.org/jessie/desklaunch).


## System Trays {#systrays}

The [freedesktop](http://www.freedesktop.org/) compatible application
can use a _systray_ as provided by gnome and kde.  Some light window
managers provide a _systray_ in their panel/taskbar like _fluxbox_, or
in their status-bar like _i3_
We can also use a stand alone  generic _sys-trays_.  For some I
have tried I give their memory size, this information is only
indicative as always because depending of many factors, and as some
part is shared memory, that may be yet loaded if you use the same
toolkit that your window manager, or one desktop component.

If we need to add system tray to a light wm, it should at least be
thin.

-   [trayer](https://github.com/sargon/trayer-srg) (4.4M)
    a fork of the [fbpanel](http://fbpanel.sourceforge.net/)
    systray. It is in Debian.
-   [Docker](http://icculus.org/openbox/2/docker/) comming from
    openbox dock any application into the system tray.
    It works for all NET WM compliant window managers
    It weight only 0.8M and works well. It is in debian.
    There is an alternative also in Debian
    [kdocker](https://github.com/user-none/KDocker)
    build with Qt, which has more dependencies.
-   [xfce4](http://www.xfce.org/) in xfce4-systray.
-   [stalonetray](http://stalonetray.sourceforge.net/)
    is a stand-alone system tray. It has full XEMBED support
    and minimal dependencies.
    Stalonetray works with any EWMH-compliant window manager and is in Debian.
-   [AllTray](http://alltray.trausch.us/) dock any application
    with no native tray icon into the system tray. Seems to be quite fat
    (6M), it is in debian.

Fluxbox, and i3 among the lighter wm have a systray included in the
build-in taskbar or statusbar.

## Clipboard managers {#clipboard}

The ICCCM (Inter-Client Communication Conventions Manual) standard
defines three _selections_, called _PRIMARY_, _SECONDARY_ and
_CLIPBOARD_. The _PRIMARY_ selection is conventionally used to
implement copying and pasting via the middle mouse button. The
_SECONDARY_ may be accessed by an alternate mouse action, it's use is
application dependent, the _CLIPBOARD_ is used by the copy/paste menu
in X applications, quite often bound to Ctl-X/Ctl-C Ctl-X/Ctl-V.

For emacs before v. 24  kill and yank commands used the primary
selection, not they use the clipboard.

-   Wikipedia: {{< wp "Clipboard manager" >}}
-   [freedesktop Specifications/ClipboardsWiki
    ](http://www.freedesktop.org/wiki/Specifications/ClipboardsWiki)
-   [Freedesktop clipboard specification
    ](http://standards.freedesktop.org/clipboards-spec/clipboards-latest.txt)
    present the use and recommendations for the three selections.
-   [ArchWiki: Clipboard
    ](https://wiki.archlinux.org/index.php/Clipboard)

The X11 applications  provide some tools to deal
with the selections

-   {{< man "xcutsel" >}} is used to copy the current selection into a cut
    buffer and to make a selection that contains the current
    contents of the cut buffer.
    By  default,  xcutsel  will  use the selection named PRIMARY, but
    this can be changed by the option `-selection`.
-   {{< man "xclipboard" >}} in the _x11-apps_ package is an X application to
    display the CLIPBOARD selection. Memory footprints: 4M res / 2M
    shr.

    The selection displayed by _xclipboard_ is the CLIPBOARD, *not the
    PRIMARY*.

-   {{< man "xcb" >}} allows up to 8 cut buffers to be manipulated either via
    the command line, or with the mouse in a point and click
    manner. It uses 4.1M res / 3.6M shr.

There are also some web applications that allow sharing of a pasted
data among computers or mobile platforms like
-   [wepaste.com](http://www.wepaste.com/)
-   [IPShare.net](http://www.ipshare.net/) for use on lan.

You can also use any {{< iref "clouds#pastebin" "pastebin" >}}.


Some newer command line to manage selection:

-   [autocutsel](http://www.nongnu.org/autocutsel/).
    synchronize the three selectionS; _in debian_.
-   [clipmenu](https://github.com/cdown/clipmenu)
    is a simple clipboard manager using
    {{< iref "#dmenu" "dmenu" >}}
    (or {{< iref "#rofi" "rofi" >}}) and
    {{< iref "#xsel" "xsel" >}};
    _clipmenud_ polls the clipboard every 0.5 seconds,  changes to the
    clipboard contents is writen to a cache; clipmenu reads the cache
    directory, and call dmenu to select one.
-   [xclip](http://sourceforge.net/projects/xclip/)
    is a command line interface to X selections. It is in Debian.
-   <a name="xsel"></a>[XSel
    ](http://www.vergenet.net/~conrad/software/xsel/)
    is a command-line program for getting and setting the contents of
    the X selection; by default  operates on the _primary_ selection,
    but you can also specify the _secondary_ or _clipboard_.
    It is in Debian.
-   [megahertz/clipboard-share
    ](https://github.com/megahertz/clipboard-share)
    is a node.js server and client to share clipboard between two
    computers.
-   [wincent/clipper](https://github.com/wincent/clipper)
    linux daemon that provide a service exposing the local clipboard
    to local or remote processes. It is meant to be used with tmux.
    running both locally and remotely.
-   [Exposing your clipboard over SSH
    ](https://gist.github.com/dergachev/8259104)
    explains how to copy clipboard to loacl and remote machines with
    `netcat`, `xclip`, and a reverse ssh session. In this article the
    linux reader will remplace `pbcopy` by `xclip -sel clip`.

There are also many clipboard managers:
-   [clipit](https://github.com/shantzu/ClipIt)
    is a lightweight GTK+ clipboard manager forked from
    {{< iref "#parcellite" "parcellite" >}}.
    Clipit seat in your tray, and allow to select clipboard history.
    It can also be used from the command line.
    Clipit has preferences to manage _CLIPBOARD_ and _PRIMARY_
    selections and synchronize them.
    Memory footprints: 19M res/ 17M shr or 25M / 21M. Clipit is in Debian.
-   [CopyQ](https://github.com/hluk/CopyQ)
    is a C++/QT  clipboard manager with editing, scripting and a
    command-line interface. It is in Debian, along with a
    _copyq-plugins_ package.
-   [Diodon](https://launchpad.net/diodon)
    is a vala clipboard manager for Gnome/Unity.
    It seems to have a big list of dependencies, when we don't use
    these full desktop software. It is in Debian.
-   [Glipper](https://launchpad.net/glipper)
    is a python clipboardmanager for Gnome,  Glipper appears in the
    notification area, it uses app indicator
    _seem abandoned since 2012 but still in debian stretch_.
-   [gpaste](https://github.com/Keruspe/GPaste)
    is a clipboard management system for Gnome. in Debian.
-   {{< wp "Glipper" >}} is a clipboard utility for Gnome. _in debian_.
-   [Parcellite](https://github.com/rickyrockrat/parcellite){: #parcellite}
    is a lightweight GTK+ clipboard manager
-   [qlipper](https://github.com/pvanek/qlipper)
    is the clipboard management system for QTDesktop. it is in Debian.

more applications on the ArchWiki page.

## Keyboard addons

-   [XbindKeys](http://www.nongnu.org/xbindkeys/) is a program that
    allows you to launch shell commands with your keyboard or your
    mouse under X Window. It links commands to keys or mouse buttons,
    using a configuration file. It's independant of the window
    manager and can capture all keyboard keys (ex: Power, Wake...).
    XbindKeys is actively maintained and is in debian.
-   [TrigerHappy](https://github.com/wertarbyte/triggerhappy)
    Triggerhappy is a hotkey daemon developed with small and embedded
    systems in mind. It attaches to the input device files and
    interprets the event data received and executes scripts configured
    in its configuration. It is in Debian.<br/>

    Unlike other hotkey daemons, it runs as a persistent, systemwide
    service and therefore can be used even outside the context of a
    user or X11 session It can handle any input device and might be
    useful on a headless system to use input events generated by a
    remote control (Ex. control an mpd server).
-   [Keynav](http://www.semicomplete.com/projects/keynav/)
    turns your keyboard into an fast pointer mover.
-   [Keylaunch (debian package)
    ](https://packages.debian.org/jessie/keylaunch)
    is a small utility for binding commands to a hot key. It reads a
    configuration file in .keylaunchrc. KeyLaunch uses Ctrl, Alt and
    Shift as modifier keys, the hotkey is up to the user.<br/>
    There is a [Jerko Steiner fork of keylaunch
    ](https://github.com/jeremija/keylaunch)
    which enables binding of Mod4 (windows) key.
-   [Synergy](http://synergy2.sourceforge.net/) lets you share a
    single mouse and keyboard between multiple computers with different
    OS, each with its own display,

## desktop background
You can use the following programs to set the X desktop backgound:

-   {{< man "xsetroot" >}}
-   {{< man "fbsetbg" >}}
-   Esetroot
-   wmsetbg
-   feh
-   hsetroot
-   chbg
-   {{< iref "images#imagemagick" "display" >}}
-   {{< iref "images#pqiv" "pqiv" >}}
-   xv
-   xsri
-   xli
-   xsetbg


feh, esetroot and wmsetbg support pseudo transparency


## Other components

-   [xgetc](http://code.google.com/p/xgetc/) print the pixel color (in
    hexadecimal notation) and position to stdout.  When a selection is
    made, xgetc will print the geometry of the selection.

# WM control {#wm_control}
These tools allow to control windows from an
[EWMH](# ewmh "internal reference") compliant manager.
They complement the basic utilities that can only give informations on
the window property like {{< man "xwininfo" >}} or {{< man "xprop" >}}.


-   [xdotool](https://github.com/jordansissel/xdotool/)
    simulate keyboard input and mouse activity, move and resize
    windows, etc.
    [xdotool manpage ](https://github.com/jordansissel/xdotool/blob/master/xdotool.pod)
-   [xwit](http://www.slack.com/sw/xwit-man.html)
    resize, iconify, pop, and move windows given by name or id, change
    an icon, title or name, set the screen saver going, and change
    individual key autorepeat settings, move the mouse cursor, etc.
-   [wmctrl](http://tripie.sweb.cz/utils/wmctrl/) (GPL)
    provides command line access to almost all the features defined in
    the EWMH specification. For example it can maximize windows, make
    them sticky, set them to be always on top. It can switch and
    resize desktops and perform many other operations. The last release is 1.07 from
    2005, but EWMH specification is still in use unchanged and this is a usefull program.
-   [xautomation](http://hoopajoo.net/projects/xautomation.html)
    control X from the command line, and find things on the screen The
    control interface allows mouse movement, clicking, button up/down,
    key up/down, etc.  The visgrep program find images inside of
    images and reports the coordinates, allowing programs to find
    buttons, etc, on the screen to click on.
-   [Devilspie2](http://www.gusnan.se/devilspie2/) (GPL)
    is a a window matching utility, allowing the user to perform
    scripted actions on windows as they are created. For example you
    can script a terminal program to always be positioned at a
    specific screen position, or automatically position a window on a
    specific workspace.  window matching utility, allowing the user to
    perform scripted actions on windows as they are created. For
    example you can script a terminal program to always be positioned
    at a specific screen position, or automatically position a window
    on a specific workspace.  Devilspie2 is in Debian, _active in
    2016_.
    -   [Devilspie2 Home](http://www.gusnan.se/devilspie2/)
    -   [devilspie2.git
        ](http://git.savannah.gnu.org/cgit/devilspie2.git)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
