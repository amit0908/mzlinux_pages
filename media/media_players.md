---
title: Sound and Video Players
---

See also  {{< iref "codecs" "Codecs" >}} and it's subsection
{{< iref "codecs#media_info" "Media Info" >}},
{{< iref "streaming" "Streaming" >}}, {{< iref "ffmpeg" "FFmpeg section" >}},
{{< iref "sound_edit" "Sound Edit" >}},
{{< iref "video_edit" "Video Edit" >}},

-----

# References
## Sound
-   [Sound-Playing-HOWTO
    ](http://www.tldp.org/HOWTO/Sound-Playing-HOWTO.html)
    lists applications for Linux that play various sound formats, but
    is outdated *1998*.
-   [Wikipedia list of Linux audio software
    ](http://en.wikipedia.org/wiki/Linux_audio_software),
    {{< wp "Comparison of audio player software" >}},
    [Comparison of media players
    ](http://en.wikipedia.org/wiki/Comparison_of_media_players)
    including many features,
    [Category: Linux Media Players
    ](https://en.wikipedia.org/wiki/Category:Linux_media_players)
    and {{< wp "List of Linux audio software" >}}.
-   [linux-sound.org](http://linux-sound.org/).
-   [ArchWiki list of audio applications
    ](https://wiki.archlinux.org/index.php/List_of_applications/Multimedia#Audio).
-   [Music software written in Python
    ](http://wiki.python.org/moin/PythonInMusic)
-   The [Free Software Directory](http://directory.fsf.org/)
    [Audio section
    ](http://directory.fsf.org/audio/)
    gives a list of GPL sound applications.

## DVD/CD
See also {{< iref "dvd_cd_recording" "DVD and CD recording" >}}

-   ArchWiki:
    -   [Optical disc drive
        ](https://wiki.archlinux.org/index.php/Optical_disc_drive)
        burning, playback, ripping, troubleshooting.
    -   [DVD Backup
        ](https://wiki.archlinux.org/index.php/Dvdbackup),
-   Ubuntu Help:
    -   [Cd/Dvd Burning
        ](https://help.ubuntu.com/community/CdDvd/Burning)
    -   [How do I enable restricted codecs to play DVDs?
        ](https://help.ubuntu.com/stable/ubuntu-help/video-dvd-restricted.html)
    -   [RestrictedFormats/PlayingDVDs - Community Help Wiki
        ](https://help.ubuntu.com/community/RestrictedFormats/PlayingDVDs)
-   [DVD FAQ](http://dvddemystified.com/dvdfaq.html) from
    dvddemystified.com _updated each month_
-   [imdb : internet movie database](http://www.imdb.com)

# Sound Players {#sound_players}

Some Media players can handle both video and audio, the following
players are refered to in the
{{< iref "#video_players" "Video players section" >}}:
{{< iref "#gnash" "Gnash" >}}
{{< iref "#mplayer" "Mplayer" >}},
{{< iref "#mpv" "mpv" >}},
{{< iref "#xine" "Xine" >}},
{{< iref "#videolan" "Videolan Client (VLC)" >}}

Wikipedia: {{< wp "Comparison of audio player software" >}},
[Comparison of free software for audio - Players
](https://en.wikipedia.org/wiki/Comparison_of_free_software_for_audio#Players)

[alsaplayer](http://www.alsaplayer.org/)
:   AlsaPlayer (GPL v3) <a name="alsaplayer"></a> is a PCM player. The Input Plugins include:
    MP2, MP3, WAV, CDDA, OGG, MPEG, MAD, CDDA, MikMod, and audiofile.
    The Output Plugins include: Alsa, OSS and OSS/Lite, Esound, Sparc,
    SGI, and JACK. Alsaplayer development stopped in 2004 with version
    0.99.75, but seem to begin again in 2007 with a new gtk2 interface,
    and has slept again the next year

<a href="amarok"></a>{{< wp "Amarok_(software)"  "Amarok" >}} (GPL)
:   said to be a very good audio player with a QT user interface,
    but is quite heavy and targeted to KDE. Amarok has been redesigned
    between v1.4 and v2.0, and many forks from previous version 1.4
    where done.

    -   _Amarok_ requires _KDE runtime_, which is a very heavy
        dependency, if your desktop is not KDE.
    -   {{< iref "#clementine" "Clementine" >}}
        is a fork of the version 1.4
        wich uses Qt and {{< iref "streaming#gstreamer" "GStreamer" >}},
        and so is less deeply immersed in KDE.
    -   {{< iref "#exaile" "Exaile" >}} is a GTK+ clone of amarok.
    -   _Amarok_ is the primary client for
        {{< iref "streaming#ampache" "Ampache" >}}
        this feature is not shared by the above derivatives.
    -   _Amarok_ can [play UPnP / DLNA streams
        ](https://userbase.kde.org/Amarok/Manual/Organization/Collection/RemoteCollections/UPnP)
        this feature is not shared by Clementine or Exaile.
    -   [ArchWiki - Amarok
        ](https://wiki.archlinux.org/index.php/Amarok)

     Main features:
     -   Play many formats including FLAC, Ogg, Opus, MP3, AAC, WAV,
         Windows Media Audio, Apple Lossless, WavPack, TTA and
         Musepack.
     -   Tag digital music files
     -   Search Covers and artist informations
     -   Playlist editing
     -   Display lyrics
     -   Podcast
     -   Play UPnP / DLNA streams


[Aqualung](http://aqualung.factorial.hu/home.html)
:   Aqualung (GPL) is a Gtk music player.
    Features:
    -   Play all sample-based, uncompressed formats, mod, mp3, Ogg
        Vorbis, Ogg Speex, flac, Musepack, Monkey's Audio, WavPack,
        and via ffmpeg AC3, AAC, WMA.
    -   Output on oss, jack, alsa, pulseaudio and can resample
    -   Audio CD play and ripping  with on-the-fly conversion to WAV,
        FLAC, Ogg Vorbis or CBR/VBR MP3 and tagging of the created files
    -   LADSPA plugin support.
    -   Tag editing
    -   Remote control through CLI commands

    If Aqualung has many dependancies upon sound libraries, it has
    none to desktop but Gtk. It is no longer in Debian since wheezy.

    -   [GitHub - Aqualung](https://github.com/jeremyevans/aqualung)
    -   [Aqualung Documentation
        ](http://aqualung.jeremyevans.net/manual/aqualung-doc.html).

[aRts](http://arts-project.org)
:   aRts (Analog Real-Time Synthesizer) is a sound system for KDE.
    aRts creates and processes sound using small modules that do
    certain tasks. aRts modules can create waveforms (oscillators),
    play samples, filter data, add signals, perform effects like
    delay/flanger/chorus, or output the data to a soundcard.

<a name="audacious"></a>[Audacious](http://audacious-media-player.org/)
:   Audacious is an GPL, XMMS like app written in GTK 2, that
    support nearly the same plugins. It is a fork of BMP, like are
    {{< iref "#xmms2" "xmms2" >}} and
    {{< iref "#bmpx" "Bmpx" >}}.
    {{< iref "#xmms2" "xmms2" >}}
    Other forks are build in a client-server model, but
    Audacious was first a single player, but now can be controlled
    through DBUS.
    Features:

    -   codecs support thru plugins: mp3, aac, vorbis, flac, monkey's
        audio (ape), wavpack, shorten, musepack, tta, wma, sid, alac,
        wav, midi, CD audio;
    -   output to oss4, alsa, esound, jack, pulseaudio, sndio, sdl
    -   support for transcoding and streaming.
    -   Controlled through DBUS, accept MPRIS protocol
    -   Can be controlled with Conky.
    -   Includes the client _audtool_ to sends commands to a running
        instance of Audacious.
    -   curses clients like
        [Audtty](http://audtty.alioth.debian.org/)
        and
        [comms](http://hoo.homeunix.net/~teknohog/hacks/comms/)
        (GPL).

    Audacious has a light memory footprint but seems somewhat processor
    demanding, I have no measure but I see my load average climbing
    each time I use it, more than other players.
    Auidacious is in Debian. The development seems to have slow down,
    no commit during the period 2016-2018.

    -   [Audacious Home page](http://audacious-media-player.org/),
    -   [Audacious Plugins](http://audacious-media-player.org/Plugins)
    -   [GitHub - Audacious
        ](https://github.com/audacious-media-player/audacious).
    -   [ArchWiki - Audacious
        ](https://wiki.archlinux.org/index.php/Audacious)

<a name="banshee"></a>{{< wp "Banshee_(music_player)"  "Banshee" >}}
:   An other music player using {{< iref "Streaming#Gstreamer" "GStreamer" >}} framework, but built
    upon Mono and Gtk#.

<a name="bmpx"></a>[Bmpx](http://bmpx.backtrace.info/site/BMPx_Homepage)
:   Bmpx (GPL) is based on {{< iref "streaming#gstreamer" "GStreamer" >}},
    and can be considered as a gstreamer gui. The old *Bmp* was based on xmms, but the
    present *Bmpx* was rewritten from scratch in C++ and no longer share code with
    xmms. Bmpx can play every format for which you have a gst plugin. It supports also
    MusicBrainz, Last.fm radio/scrobbling, HAL, DBus.

<a name="clementine"></a>[Clementine](http://www.clementine-player.org/)
:   Clementine is a QT fork of amarok 1.4, with which it shares main features.
    {{< wp "Clementine_(software)"  "Wikipedia: Clementine" >}}.
    Clementine can play internet streams, transcode music into MP3, Ogg Vorbis, speex,
    FLAC or AAC, manage tags, use CUE sheets, be controlled from android phone, and many
    [features](http://www.clementine-player.org/about), playing main
    formats included opus, and can read all playlists including cue sheets but has no
    bookmark nor access to chapters. With one ogg file loaded it uses
    85M resident / 60M shared.

    -   [Controlling Clementine from the commandline with DBus and MPRIS
        ](https://github.com/clementine-player/Clementine/wiki/Controlling-Clementine-from-the-commandline-with-DBus-and-MPRIS)

<a name="exaile"></a>[Exaile](http://www.exaile.org/)
:   [Exaile](http://en.wikipedia.org/wiki/Exaile)
    (GPL) is an audio player written in python using pygtk and using
    {{< iref "streaming#gstreamer" "GStreamer" >}}
    aiming to be similar to KDE's AmaroK, but for GTK+. It has a plugin system that
    allow: MPRIS control
    ([mpris plugin
    ](https://github.com/exaile/exaile/tree/master/plugins/mpris)),
    bidirectional last.fm support, a shoutcast directory browser, tag
    editing thru an
    {{< iref "tag_management#mutagen" "ExFalso" >}}
    plugin, {{< iref "streaming#daap" "DAAP protocol" >}}
    _client and server_ support.  As a PyGTK player you can expect a memory footprint of
    81M/39M shared (one ogg file loaded). Exaile is no longer in Debian since _jessie_.

    -   [GitHub - Exaile](https://github.com/exaile/exaile)
    -   [Exaile Documentation](http://exaile.readthedocs.io/en/stable/)
    -   [ArchWiki - Exaile
        ](https://wiki.archlinux.org/index.php/Exaile)


[Gradio](https://github.com/haecker-felix/gradio)
:   Gradio is a GTK3 app for finding and listening to internet radio stations.
    [ArchWiki - Gradio](https://wiki.archlinux.org/index.php/Gradio)


[Goggles Music Manager](https://gogglesmm.github.io/)
:   is a music collection manager and player. It is written in C++, and uses a sqlite
    database, the xine library for playback and the
    [FOX Toolkit](http://www.fox-toolkit.org/) for the interface.
    </br />
    It categorizes your music files based on genre, artist, album, and song.  It
    supports gapless playback and tag editing.  It supports Ogg Vorbis , FLAC, MP3 ,
    MP4, ASF and Musepack music files.<br />
    As it uses a desktop agnostic UI it has limited dependencies.

    -   [GitHub: goglesmm](https://github.com/gogglesmm/gogglesmm)

<a name="guayadeque"></a>[Guayadeque](http://guayadeque.org/) (GPL)
:   Guayadeque is an audio player with database written in C++. It uses
    {{< iref "streaming#gstreamer" "GStreamer" >}}
    and _wxWidgets_ for the UI. It can play Ogg Vorbis, FLAC, MP3 or anything supported
    by _gstreamer_.  It can be interfaced through MPRIS D-Bus interface.  _in Debian_.

    -   Wikipedia: {{< wp "Guayadeque Music Player" >}}.

{{< iref "#mplayer" "mplayer" >}}
:   MPlayer is a movie player. It plays most video and **audio**
    formats. He is described in the
    {{< iref "#mplayer" "Video Players section" >}} MPlayer can be used to
    record streaming audio with a command line like:
    `mplayer -playlist playlist.txt -ao pcm -aofile mystream.wav -vc dummy -vo null`
    It can be used from a cron tab like:
    `0 11 * * 1-5 /home/username/scripts/streamrecorder >& /dev/null 0 14 * * 1-5 killall -9 mplayer`

{{< iref "#mpd" "Music Player Daemon" >}}
:   has a subsection.

{{< wp "Muine" >}}
:   An other music player using {{< iref "streaming#Gstreamer" "GStreamer" >}}
    framework, but built upon Mono and Gtk# (like _Banshee_), not used on my systems.

<a name="qmmp"></a>[Qmmp](http://qmmp.ylsoftware.com/) (GPL)
:   _Qmmp_ is a C++/QT audio player. Qmmp is in Debian.
    On amd64 _Qmmp_ footprints are 70M res / 50M shr when playing an
    ogg file_in may 2018 with _Qmmp 1.2.0_.


    Features:

    -   Codecs:  any formats provided by libsndfile, or ffmpeg
    -   Codecs list: MPEG1 layer 2/3, Ogg Vorbis, Ogg Opus,
        Native FLAC/Ogg FLAC, Musepack, WavePack,
        tracker modules (mod, s3m, it, xm, etc), ADTS AAC, CD Audio,
        WMA, Monkey's Audio, PCM WAVE, Midi, SID, Chiptune formats.
    -   DSP effects with LADSPA
    -   Output to OSS4, Alsa, Pulse Audio, Jack, QtMultimedia,
        Icecast
    -   MPRIS (1.0 and 2.0)
    -   Cue sheet
    -   Lyrics
    -   [Extra plugins](http://qmmp.ylsoftware.com/links.php)


<a name=quodlibet></a>[QuodLibet](http://code.google.com/p/quodlibet/)
:   Quod Libet (GPL) is a GTK+-based audio player written in
    Python. It uses
    {{< iref "streaming#gstreamer" "gstreamer" >}}
    and supports Ogg Vorbis, FLAC, MP3, Musepack/Wavepack,
    MOD, MP4, TrueAudio, WMA.<br /> _QuodLibet_ uses playlists based
    on regular expressions and can display and edit tags.

    As other PyGTK players _like {{< iref "#exaile" "Exaile" >}}
    __QuodLibet__ is quite memory hungry (52M resident when playing mp3) as is ExFalso
    and if you are not using a full gnome desktop, you need to avoid _python-gnome2_
    otherwise you pull all the libraries and daemons.

    Even if we can find _QuodLibet_ too big as a background player, it is a nice tool
    for the _listen then tag_ game _like its brother _{{< iref "#exaile" "Exaile" >}}_.

    __Quodlibet__ use the python library {{< iref "tag_management#mutagen" "mutagen" >}}
    and share code with the {{< iref "tag_management#exfalso" "ExFalso" >}} tag editor.

    -   [ExFalso/Quodlibet manual](https://quodlibet.readthedocs.org/en/latest/)


[RealPlayer](http://www.real.com/linux) and [Helix Player](https://helixcommunity.org/)
:   Helix player is an open source media player, with support for
    the proprietary format `RealAudio` and `RealVideo` it is known as
    the proprietary RealPlayer. Mplayer is also known to play real
    audio and video with the appropriate codec. A test page for real
    audio and video streams is the
    [RealAudio and RealVideo Test Clips
    ](http://service.real.com/realplayer/test/)

<a name="rhythmnbox"></a>[Rhythmbox](http://en.wikipedia.org/wiki/Rhythmbox)
:   [Rhythmbox]((https://wiki.gnome.org/Apps/Rhythmbox)
    (GPL) is a gnome audio player using the
    {{< iref "streaming#gstreamer" "GStreamer" >}} media framework.

    Main features:
    -   play streamed Internet radio and podcasts
    -   playlist
    -   gapless playback
    -   Audio CD ripping
    -   Album cover display
    -   Song lyrics display
    -   Scrobbling
    -   DAAP  via DAAP sharing plugin which uses libdmapsharing.
    -   UpNP through [Grilo](https://developer.gnome.org/grilo/)
        plugin. _On Debian the package grilo-plugin is needed_.
    -   can subscribe to podcasts
    -   Web Remote Control[edit]
    -   Plays ampache streams through a plugin.
    -   Numerous [plugins
        ](https://en.wikipedia.org/wiki/Rhythmbox#Plug-ins)
        including [Third party plugins
        ](https://wiki.gnome.org/Apps/Rhythmbox/Plugins/ThirdParty).

    Rhythmbox playing a single small mp3 take 90M res / 50M shr (on
    amd64 in may 2018)

    -   [ArchWiki - Rhythmbox
        ](https://wiki.archlinux.org/index.php/Rhythmbox)


[xmcd & cda](http://www.amb.org/xmcd/)
:   Xmcd is a full-featured CD Player and Ripper, cda is a shell
    command-line utility which also features a curses-based,
    screen-oriented mode. xmcd is an alsa compatible application

<a name="xmms2"></a>[Xmms2](http://wiki.xmms2.xmms.se/index.php/Main_Page)
:   XMMS2 (GPL) is a music player developped using the
    client-server model which will provide kde, gtk, and command-line
    interface.
    It replaces the old _Xmms_ which was unmaintained and is sticked to gtk-1,
    It can play mp3, vorbis, aac, alac, wma, mac, sid, mod,
    wav, flac, mpc, speex files. It is provided as a daemon with
    numerous plugin packages and client.

    __xmms2__ has numerous clients
    graphic ones for gtk or kde, command line and ncurses clients, and
    also webclient that allow to control the daemon from a remote
    device. They are listed on the
    [Client page of xmms2 wiki](http://wiki.xmms2.xmms.se/wiki/Clients).

    The daemon itself is small 4.5M, and clients are 11M for gxmms2,
    14M for xmms2tray, wmxmms2 is only 1.7M and is the great winner
    among the graphic clients.

    We can also dispense with graphic gadgets
    and use the [console or command line client
    ](https://xmms2.org/wiki/Clients#Console_Clients) starting with _nyxmms2_
    the standard console application coming with XMMS2
    and use no permanent resource at
    all when you use it only to launch, pause or stop the daemon, and
    only up to 1M is you let the status run on a permanent basis. In
    the same way a web client will use very few resources if running as
    a cgi script.

    Support for music formats/protocols is done through
    [plugins](https://xmms2.org/wiki/Plugins). There is a transport
    plugin for DAAP protocol, it is packaged in Debian as
    _xmms2-plugin-daap_.


## Text Players

<a name="audiopreview"></a>
[audiopreview](http://audiopreview.codealpha.net/audiopreview/)
:   is a simple command line tool based on
    {{< iref "streaming#gstreamer" "gstreamer" >}}
    to play previews of audio and video
    files, and internet streams. It can also be used as a
    regular media player. It is no longer in Debian since jessie,
    and the home page went away.

auditive
:   [auditive](http://www.rillion.net/auditive/)
    is a ncurses {{< iref "streaming#gstreamer" "GStreamer" >}} player written in vala.
    _last release 2013_.

cdtool
:   cdtool ([cdtool(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=cdtool%281%29))
    contains
    several programs for playing audio CDs and controlling a CD-ROM
    drive from the command line:

:   -   [cdplay](http://www.x-paste.de/cdplay/) is an interactive
        text-mode program for playing audio CDs. ref:
        [cdplay(1)
        ](http://manpages.debian.org/cgi-bin/man.cgi?query=cdplay%281%29)
    -   The _cdinfo_ command, with no option used, will print out the
        audiostatus.
    -   The _cdstop_ command stops the compact disc.
    -   The _cdpause_ command pauses the currently playing compact disc.
        Resume by using cdplay with no arguments.
    -   The _cdvolume_ command sets the output volume level (an integer
        from 0 to 255) of the CD player.
    -   The _cdir_ command lists information about the currently loaded
        audio compact disc. It lists the lengths of all tracks. It can also
        references a database files to find title, artist, and track name
        information.
    -   The _cdeject_ command ejects the current compact disc and the
        cdclose command closes the CDROM tray.


[cdparanoia](http://www.xiph.org/paranoia/)
:   Cdparanoia (Paranoia III) reads digital audio directly from a
    CD, then writes the data to a file or pipe in WAV, AIFC or raw 16
    bit linear PCM format. Cdparanoia does various extra checks and
    should be preferred to cdda2wav used when a perfect copy is
    necessary, or when the disk media or drive is damaged. cdparanoia
    can find if the paranoid tests are necessary or if the plain
    [cdda2wav can work with the cdrom](http://www.xiph.org/paranoia/faq.html#ok).
    refs: [cdparanoia(1)](http://www.xiph.org/paranoia/manual.html),
    [cdparanoia FAQ](http://www.xiph.org/paranoia/faq.html),
    [cdparanoia troubleshooting](http://www.xiph.org/paranoia/trouble.html)


cdda2wav
:   [cdda2wav(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=cdda2wav%281%29)
    is a sampling utility for CD-ROM (see
    {{< iref "sound_edit#cdda2wav" "cdda2wav entry in the Sound Editors, recorders section" >}}),
    it can also be used as a CD player.

[Cjukebox](http://muth.org/Robert/Cjukebox/)
:   is a GPL Python/Curses based management system for audio files
    and playlists, it uses [Musicus](http://muth.org/Robert/Musicus/)
    that uses xmms plugins in a non X environment. Development stalled
    since 2005


<a name="cmus"></a>[cmus](https://cmus.github.io/) (GPL)
:   cmus (GPL) is a ncurses text player.

    Main Features:

    -   Can play mp3, ogg/vorbis, FLAC, Opus, Musepack, WavPack, WAV,
        AAC, MP4, audio CD, and everything supported by ffmpeg (WMA, APE,
        MKA, TTA, SHN, ...) and libmodplug
    -   Tiny cmus 2.7.0 is 24M res. / 17 shr on amd64 (may 2018)

    Cmus has uncommon key binding and unusual help system: you have to
    type 7 to get help on key-bindings, to know you have to type 7,
    you just need hit the 7 key! Of course q does not quit, h or ?
    does not give help. But to be fair I must say that you are free to
    configure key-bindings as you want. It is in active development in
    2018 and packaged in Debian.

    -   [GitHub cmus repository
        ](https://github.com/cmus/cmus)
    -   [cmus wiki](https://github.com/cmus/cmus/wiki)
    -   Wikipedia {{< wp "Cmus" >}}
    -   [ArchWiki - Cmus](https://wiki.archlinux.org/index.php/Cmus)

[Herrie](https://github.com/EdSchouten/herrie) (BSD Licence)
:   Herrie is a minimalistic command line music player. It supports wav,
    ogg, flac, mp3 and playlist (XSPF), it is 5.8M resident when
    playing mp3.


MikMod
:   MikMod ( [mikmod(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=mikmod%281%29))
    is a MOD
    music file players for UNIX-like systems. MikMod uses the OSS
    /dev/dsp driver included in all recent kernels for output, and will
    also write .wav files. Supported file formats include MOD, STM,
    S3M, MTM, XM, ULT, and IT. The player uses ncurses for console
    output and supports transparent loading from gzip/pkzip/zoo
    archives and the loading/saving of playlists.


<a name="madplay"></a>[madplay(1)
](http://manpages.debian.org/cgi-bin/man.cgi?query=madplay)
:   madplay is a command-line MPEG audio decoder and player based
    on the  MAD library
    {{< iref "sound_libs#item_libmad" "libmad" >}} and the
    [Mad audio decoder](http://www.underbit.com/products/mad/).
    madplay reads and decodes one or more input files containing MPEG
    audio data and plays them on the native audio device. It can also
    output a sound file in cdda, aiff, wave, snd, esd, raw
    formats. _see  [madplay(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=madplay(1))


<a name="moc"></a>[Moc](http://moc.daper.net/)
:   Moc (GPL)
    ([Moc wikipedia page](http://en.wikipedia.org/wiki/Music_On_Console))
    is an ncurses-based console audio player with ALSA, OSS or JACK
    outputs.
    Supported file formats are: mp3, Ogg Vorbis, FLAC, Musepack (mpc),
    Speex, WAVE,  AIFF, AU, SVX, Sphere Nist WAV, IRCAM SF, Creative VOC
    with the  FFmpeg plugin we add  (WMA, RealAudio, AAC, MP4).
    _Moc_ works as a daemon and can be controlled by a command line or
    via conky, but it is not usable thru the network like the music
    servers {{< iref "#mpd" "Mpd" >}} or
    {{< iref "#xmms2" "Xmms2" >}}. It uses 6M resident.

   -   [MOC Readme](http://moc.daper.net/node/87)
   -   [Python Music On Console](http://moc.lophus.org/)
       is a wrapper around moc.
   -   [ArchWiki - Moc](https://wiki.archlinux.org/index.php/Moc).

<a name="mpg123"></a>{{< wp "Mpg123" >}}
:   Mpg123 (LGPL) is a very fast decoder and player for mp3 _or any
    MPEG 1.0/2.0/2.5 stream (layers 1, 2 and 3)_ running on
    unix and w32 it support a lot aof audio interfaces including alsa,
    coreaudio, esound, jack, nas, oss, portaudio, pulseaudio, SDL.
    It  can also play MPEG audio files from a WWW server.
    _[mpg123(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=mpg123(1))

    [Mpg321](http://sourceforge.net/projects/mpg321)<a name="mpg321"></a>
    is a GPL replacement
    for Mpg123 which aimed at a truly free software mp3 player, while
    previous versions of mpg123 did not have a clear free opensource license.
    [mpg321(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=mpg321(1))

    There are some controversies about the respective performance of mpg123
    and mpg321. I have even read that mpg123 is twenty time faster. I made
    some test on an  Intel Core 2 Duo CPU  @ 2.00GHz, and found that
    mpg321 _(mpg321  0.2.10)_ is 16% slower than mpg123 _(mpg123 1.4.3)_.
    Of course it does not presume what it could be on other platforms.

    One other aspect of comparing both decoders is on memory footprint.
    when decoding a 42mn mp3 stream _(32kHz 128b/s)_ the resident size of
    mpg321 climbed progressively up to 36M, while mpg123 staid at 1M
    resident.

    Of course {{< iref "#madplay" "madplay" >}} that is based on the same libmad library
    has analogous performance in term of speed and memory fottprints, than mpg321.
    _It should be slower because doing only fixed arithmetic,
    but I found it 10% faster on an intel dual core._


<a name="mp3blaster"></a>[mp3blaster](http://mp3blaster.sourceforge.net/)
:   An interactive text-console based ogg, mp3, sid and wav player, with
    playlist management. As a ncurses application his memory
    requirements are low 3.5M resident. refs:
    [mp3blaster(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=mp3blaster%281%29)
    ,
    [splay
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=splay%281%29)
    ,
    [nmixer(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=nmixer%281%29)


mpd text clients
:  {{< iref "#mpd" "mpd" >}} can be controlled by text clients
   like mpc, ncmpc, bash mp; they are referenced in the
   {{< iref "#mpd" "mpd section" >}}.


__ogg123__, __oggdec__
:  both GPL,  are part of the _vorbis tools_ which are the command lines utility
   of the {{< wp "Vorbis" >}} reference implementation, other decoders for
   ogg-vorbis are [Tremor](http://wiki.xiph.org/Tremor "wiki.xiph.org Tremor"),
   [Tremolo](http://wss.co.uk/pinknoise/tremolo/ "wss.co.uk pinknoise/tremolo")
   (GPL) _for arm platforms_ and ffmpeg _(see
   {{< iref "video_edit" "Video Encoders" >}}_.

   Performance of compression and quality  of _vorbis_ and mp3 are
   available in quantity and number, _(look on
   {{< wp "Vobis"  "Wikipedia:   Vorbis page" >}})_ but we compare less often
   speed and memory footprint. I compared _oggdec_ ,_mpg123_ and
   _mpg321_ on an intel dual core 2GHz, for the same wave file encoded
   at similar compression rate. I found _oggdec_ 20% slower than the
   mp3 decoders, a result not so significative, considered that I
   tried only on one stream. More interesting _oggdec_ and _mpg123_ stayed
   at 1.2Mb and 1Mb of resident memory, while _mpg321_ went up to 36Mb.


[Plait](http://stephenjungels.com/jungels.net/projects/plait/)
:   A command-line jukebox and music player front end. It can play a
    single song, mix queries that combine works from multiple artists,
    stream queries that find Shoutcast radio streams.  Plait
    automatically hands off a play list to one of the supported music
    players (or you can use it manually with any player that supports
    .m3u playlists). It is in Debian.


[play]( http://git.sysphere.org/play/)
:   A curses front-end written in python for various audio players based
    on cplay.

[PyTone](http://www.luga.de/pytone/)
:   is a GPLv2 music jukebox written in Python with a curses based
    GUI. I had no opportunity to try v3.0.0 which freeze when trying to
    index my sound library.


[Orpheus](http://thekonst.net/en/orpheus)
:   is a GPL text mode menu- and window-driven audio player
    application for CDs, internet stream broadcasts and files in MP3
    and Vorbis OGG format. It is in debian.

[Radiotray](http://radiotray.sourceforge.net/)
:   is a simple music streaming player that lives on the system
    tray. By clicking on the RadioTray icon, you'll be presented with
    a list of pre-configured online radios. By selecting one of those
    radios, it will start playing. Radiotray is in Debian.
    -   [ArchWiki - Radiotray
        ](https://wiki.archlinux.org/index.php/Radiotray)

[Sotetsu](http://code.google.com/p/sotetsu/) (GPL)
:   Sotetsu is a Terminal-based music plyaer written in Python3.x
    using Digital Audio Access Protocol (DAAP).
    The script has been written in 2009, and not updated.


## Emacs controlled Players {#emacs_players}

See also [EmacsWiki: MusicPlayers](http://www.emacswiki.org/emacs/MusicPlayers)

[Bongo](https://github.com/dbrock/bongo/) (GPL)
:   Bongo is a music player for emacs that was developped in parallel
    with EMMS. Bongo it can use VLC,
    mpg321, ogg123, speexdec. Bongo has an
    [emacswiki page](http://www.emacswiki.org/emacs/Bongo).


[EMMS](http://www.emacswiki.org/cgi-bin/emacs.pl/EMMS) (GPL)
:   EMMS (GPLv3) is the Emacs Multi-Media System, a small
    application to play multimedia files from Emacs using external
    players. It can use mpg321, ogg123, mplayer, xine or
    {{< iref "#mpd" "mpd" >}}, or any simple player available as unix command
    line client.

<a name="libmpdee"></a>[libmpdee](https://github.com/andyetitmoves/libmpdee) (GPL)
:   LMibmpdee    is a client library for  {{< iref "#mpd" "mpd" >}}
    in emacslisp, packaged in MELPA.

[simple-mpc](https://github.com/jorenvo/simple-mpc) (GPL)
:   A GNU Emacs frontend to mpc, packaged in MELPA.

[Mingus](http://github.com/pft/mingus) (GPL).
:   Mingus is an extension of {{< iref "#libmpdee" "LMibmpdee" >}}
    by Niels Giesen, packaged in MELPA.  The interface resembles that of
    {{< iref "#ncmpc" "ncmpc"  >}}, and it provides extensive playlist editing
    facilities. It can be interfaced from emacs-w3m an dired.  _mingus stays home_ is
    used to play any local sound files, it provides a cd-burning tool
    and tag editing with [taggit]( https://github.com/ft/taggit).

[MonK](http://www.asahi-net.or.jp/%7Epi9s-nnb/monk/)
:   is an emacs player for cd audio, mp3, mpg video. Don't seem any
    longer maintained since 2003

__MPC__
:   is major mode providing an interface to MPD bundled with
    Emacs >= 23.2 .

[mpdel](https://gitea.petton.fr/mpdel/mpdel) (GPL)
:   Emacs user interface for Music Player Daemon, Available from melpa.

[simple-mpc](https://github.com/jorenvo/simple-mpc) (GPL)
:   A GNU Emacs major mode that acts as a front end to mpc.
    it is in Elpa.

# Music Player Daemon {#mpd}
## MPD Server

[Music Player Daemon](http://en.wikipedia.org/wiki/Music_Player_Daemon)
Music Player Daemon or MPD (GPL)allows remote access for
playing music  and managing playlists.

-   MPD can play MP3, Ogg Vorbis, Opus,FLAC, AAC, Mod, Musepack,
    Wavepack, wave files or anything produced by FFmpeg. More
    precisely it can play anything decoded with a [decoder plugin
    ](https://www.musicpd.org/doc/user/decoder_plugins.html): adplug,
    audiofile, faad, ffmpeg, flac, dsdiff, dsf, fluidsynth, mad,
    mikmod, modplug, mpcdec, mpg123, opus, pcm, sidplay, sndfile,
    vorbis, wavpack, wildmidi.
-   The input are not limited to files but can also come from any
    [input plugin
    ](https://www.musicpd.org/doc/user/input_plugins.html):
    alsa input from a soundcard, CD audio, HTTP stream with curl; rtp
    / rtsp / rtmp / rtmpt / rtmps with ffmpeg; unmounted smb or nfs,
    upnp servers on the local network, some commercial streaming services.
-   MPD can resample the input with a [resampler plugin
    ](https://www.musicpd.org/doc/user/resampler_plugins.html) i.e.
    either the internal resampler of low quality, but low cpu load; or
    better with libsamplerate or soxr.
-   MPD can then reencode the stream with an [encoder plugin
    ](https://www.musicpd.org/doc/user/encoder_plugins.html)
    null _i.e. no rencoding_, flac, mp3 with lame or shine, mp2 with
    twolame, opus, or vorbis for ogg vorbis, wave.
-   MPD can use any type of playlist with the [playlist plugins
    ](https://www.musicpd.org/doc/user/playlist_plugins.html)
    .asx, .cue,  embedded CUE sheets from the "CUESHEET" tag with the
    embcue plugin, .m3u, extm3u, cuesheet metablock from a FLAC file
    with the flac plugin, .pls, .rss, playlist from SoundCloud,  XSPF
    playlists.
-   Mpd can output to alsa, or Jack and can send
    it's output thru network by using the {{< iref "sound_libs#libao" "libao" >}}
    and {{< iref "streaming#item_esound" "esound" >}} or
    {{< iref "streaming#pulseaudio" "use PulseAudio" >}}.
    The choice is down by setting
    [configuration options](https://www.musicpd.org/doc/user/config.html).
-   By using {{< iref "streaming#pulseaudio" "pulseaudio-dlna" >}}
    MPD can act as a UPnP / DLNA server.
-   MPD has its own [HTTP streaming server
    ](https://wiki.archlinux.org/index.php/Music_Player_Daemon/Tips_and_tricks#HTTP_streaming)
    capable of producing Ogg Vorbis and MP3 HTTP streams.
-   Mpd can output to an icecast or shoutcast server with the
    [shout ouput plugin
    ](https://www.musicpd.org/doc/user/output_plugins.html#shout_output)
    as described in
    [ArchWiki - Icecast: Streaming with MPD
    ](https://wiki.archlinux.org/index.php/Icecast#Streaming_with_MPD).
    but the native MPD streaming server can be preferred.

-   [MPD User documentation](https://www.musicpd.org/doc/user/)
-   [mpd(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=mpd%281%29)
-   [MPD configuration example
    ](https://github.com/MusicPlayerDaemon/MPD/blob/master/doc/mpdconf.example)
-   [GitHub - MPD](https://github.com/MusicPlayerDaemon/MPD)
-   [ArchWiki: Music Player Daemon](https://wiki.archlinux.org/index.php/Mpd)
-   [ArchWiki: MPD Tips and tricks
    ](https://wiki.archlinux.org/index.php/Music_Player_Daemon/Tips_and_tricks)
-   [ArchWiki - Music Player Daemon/Troubleshooting
    ](https://wiki.archlinux.org/index.php/Music_Player_Daemon/Troubleshooting)
-   [Gentoo Wiki- MPD](https://wiki.gentoo.org/wiki/MPD)
    gives the configuration for a Bluetooh headset.
    See also
    [Gentoo Wiki - Bluetooth Headset](https://wiki.gentoo.org/wiki/Bluetooth_Headset).
    and the {{< iref "bluetooth" "Bluetooth section" >}}.

-   xmms2 team has published a
    [comparison of xmms2 and mpd
    ](https://xmms2.org/wiki/XMMS2_vs_MPD),
    may be slightly biased in favor of {{< iref "#xmms2" "xmms2" >}},
    it omits that _mpd_ is
    lighter in memory and cpu than xmms2, and also that if the client
    development effort of {{< iref "#xmms2" "xmms2" >}}
    is presently greater than the older
    _mpd_, _mpd_ has still more language bindings and clients. In any case
    both server are worthwhile to try.
-   mpd can be controlled by a {{< iref "sound_libs#mpris" "MPRIS" >}} client
    through the [mpDris2](https://github.com/eonpatapon/mpDris2)
    <a name="mpdris2"></a> daemon that is run in the user session and
    monitors a local or distant mpd server.

## Clients
Mpd has
[client libraries](http://mpd.wikia.com/wiki/Client_Libraries)
in C/C++, Java, lisp/scheme, haskell, perl, php, python, Ruby.

For python you fin two main libraries:

-   [python-mpd](http://pypi.python.org/pypi/python-mpd/)
    is the older recommended library.
-   [python-mpd2](https://pypi.python.org/pypi/python-mpd2/)
    is an improvement of python-mpd.


The [MPD Manual](http://www.musicpd.org/doc/user/) has a a
[Configuration chapter](http://www.musicpd.org/doc/user/ch03.html).

You find a [long list of MPD clients in the mpd wiki
](http://mpd.wikia.com/wiki/Clients), most of
them are in the [mpd git repository](http://git.musicpd.org/),
the list is not always up-to date and some software are obsoletes.

A selection of clients:

-   {{< iref "streaming#ampache" "Ampache" >}}
    A  stream server for (see the {{< iref "streaming#ampache" "Ampache entry" >}})
    That can control many mpd instances for local play.
-   [Ario](http://ario-player.sourceforge.net/) a GTK2 client for _mpd_
    and {{< iref "#xmms2" "xmms2" >}}  inspired by Rhythmbox.
    _17M resident 10M shared_.
-   {{< iref "monitoring#conky" "Conky" >}}
    the monitoring daemon has a plugin to display the mpd state.
-   [emms](http://www.gnu.org/software/emms)
    the emacs multimedia player, can control mpd.
-   [fookebox](https://github.com/cockroach/fookebox/)
    is a jukebox-style web-frontend to mpd written in python
    with the pylons framework. It is in debian.
-   [Gimmix](https://github.com/cmende/gimmix) is a
    graphical client written in C using GTK+2. It supports playlist
    management and ID3v2 Tag editing. _20M resident including 12M shared_
-   [Guimup](http://www.coonsden.com/) a client
    written in C++ and GTKmm.
-   [glurp](http://sourceforge.net/projects/glurp/)
    Graphical interface written in GTK+ (10M resident, 8.5M shared
    ).  [GitHub: glurp](http://git.musicpd.org/cgit/master/glurp.git/)
-   [gmpc](http://gmpc.wikia.com/wiki/Gnome_Music_Player_Client)
    Gnome Music Player Client with playlist and tag management. It is
    a GTK client with light gnome dependencies (13M resident,10M, 3M
    added on my sys. ).
-   {{< iref "streaming#jinzora" "Jinzora" >}}
    A web based streaming and media management system.
-   _mpc_ the reference (Scriptable) command
    line client provided with _mpd_.
    Refs: [mpc(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=mpc%281%29)
-   __MPC.el__ is major emacs mode providing an interface to MPD.
-   [MPDCon](http://www.nongnu.org/gap/mpdcon/index.html) - A
    Graphical interface built with GNUstep SQLClient library.
-   [mpd remote](https://iprog.com/projects)  very basic PHP client
    designed for a mobile phone's browser.
-   [Mpd WebAmp](http://cseickel.googlepages.com/mpdwebamp)
    (GPL) is a web client for mpd based on turbogears.
-   [musicpm](http://code.google.com/p/musicpm/)
    is a firefox extension written with the xul library it communicates
    with MPD over TCP sockets.
-   [ncmpc](http://git.musicpd.org/cgit/master/ncmpc.git/) -
    ncurses console client (1.6M resident, 1.2 shared) Refs:
    [ncmpc(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=ncmpc%281%29)
-   [ncmpcpp](http://ncmpcpp.rybczak.net/) is a rewrite in C++ and  of
    ncmpc, with some added features. It is _in 2018_ a very actively
    maintained, and updated project.
    -   [ArchWiki: Ncmpcpp
        ](https://wiki.archlinux.org/index.php/ncmpcpp)
    -   [GitHub - jelly/ncmpcpp-cheatsheet
        ](https://github.com/jelly/ncmpcpp-cheatsheet)
-   [phpMpReloaded](http://phpmpreloaded.sourceforge.net/) Group four
    Web interfaces  written in PHP with or without javascript:
    _PhpMp_ a simple web interface,  _PhpMp2_ add themes,
    _phpMp+_ is an enhanced PHP web
    interface with javascript that fit in your web browser's sidebar,
    _phpMp3_ is totally in JavaScript,
    driven by XMLHTTPRequest (AJAX) with a small php-backend, _iPodMp_ a
    php/ajax client, optimized for Apple's iPhone & iPod,
    _MPD-Web-Remote_  a mobile client for iPhone/iPad.
-   [Pitchfork MPD client](http://sourceforge.net/projects/pitchforkmpd/)
    is an ajax/php webinterface to mpd with optional streaming with
    icecast. _last release 2009_. There are some fork _patchfork_ that
    is no longer developed since 2010, and _web-mpd_.
-   [Pympd](http://pympd.sourceforge.net/) a frontend for mpd in
    the style of rhythmbox and itunes, written in python, with pygtk.
    (18M resident, 11M shared, on my system 7M truly
    added). _Unmaintained since 2007_.
-   [RDMPD](https://github.com/desfrenes/RMPDC) a simple PHP client
    targeted to smartphone with a basic browser (no javascript).
    _Last update 2010_
-   [Sonata](https://github.com/multani/sonata) is a e
    GTK+ client, a continuation of the unmaintened *Pygmy* client with
    playlist, tagediting, stream and Audioscrobbler (last.fm) support.
    (21M resident, 11M shared)
-   [Theory](http://theory.steelbreeze.org/)
    web based MPD client based on Python, pylons, and python-mpd.
-   [vimpc](https://github.com/boysetsfrog/vimpc) (GPL)
    A curses based client with vi like key bindings .
-   [WMmp](http://git.musicpd.org/cgit/master/wmmp.git/) - Window Maker
    dockapp
-   [wymypy](http://manatlan.infogami.com/wymypy)
    an http wsgi server written in python featuring a mpd client.
    It is an old unmaintained client with a fork in
    [GitHub: 02strich/wymypy
    ](https://github.com/02strich/wymypy).
-   [ympd
    ](https://github.com/notandy/ympd)
    is a tiny web client written in C with no other dependency than
    libmpdclient 2.

## Mpd bookmarks

To use bookmarks in mpd we can use

-   Joey Hess has set
    [mpdtoys](http://git.kitenet.net/?p=mpdtoys.git;a=tree),
    which is a collections of perl scripts for mpd. He [explains
    how he use them](https://joeyh.name/blog/entry/my_mpd_setup/).
    _mpstore_, and _mpdload_ which dumps and restore the mpd daemon
    state can be used with audiobooks.
-   [MPD Bookmark](https://github.com/RaoulChartreuse/mpd_bookmark)
    is a simple script witch monitor MPD and keep a trace of where
    the listening of a file ended.
-   [mpdmark](https://github.com/Mic92/mpdtools) by Jörg Thalheim
    is a python script to bookmark songs, The author has also written
    [mpstated](https://github.com/Mic92/mpdstated) a vala program
    which restore recent position for each podcast in mpd.


# Video Players {#video_players}

All
{{< iref "streaming#upnp_media_clients" "UPnP media clients" >}},
all {{< iref "#media_centers" "media centers" >}},
and many of the
{{< iref "streaming" "Music Streamers" >}}
can also stream video,
so you can also look around in these sections.

Of course video players allow also to play music, for other sound
players see the {{< iref "#sound_players" "Music Players section" >}}.

Wikipedia has a big
[Comparison of media players
](http://en.wikipedia.org/wiki/Comparison_of_media_players)
including many features,
a [Category: Linux Media Players
](https://en.wikipedia.org/wiki/Category:Linux_media_players)
and a page {{< wp "List of Linux audio software" >}}.


## Gstreamer {#gstreamer}

GStreamer (LGPL) is a streaming-media framework, based on graphs of filters
which operate on media data. Applications using this library can do
anything from real-time sound processing to playing videos.it is
{{< iref "streaming#gstreamer" "referenced in the Music Streamer section" >}}

## [Gnash](http://gnashdev.org/) {#gnash}

Gnash (GPLv3) is the GNU Flash movie player which can be run
standalone, as well as as a plugin for several browsers. Gnash can use
either {{< iref "streaming#gstreamer" "GStreamer" >}} or ffmpeg as codec support library.

## [Lightspark](https://github.com/lightspark/lightspark) {#lightspark}
__Lightspark__ (GPL) is a Flash player implementation that run as a
web browser plugin or as a standalone application.
_LightSpark_ is in Debian.

-   [Lightspark GitHub repository
    ](https://github.com/lightspark/lightspark)
-   [Lightspark Wiki
    ](https://github.com/lightspark/lightspark/wiki/)
-   [Lightspark Support for various websites
    ](https://github.com/lightspark/lightspark/wiki/Site-Support)

## MPlayer  {#mplayer}

[Mplayer](http://www.mplayerhq.hu/) (GPL) is a movie player. It plays most video formats
as well as DVDs.  Its big feature is the wide range of supported output drivers.

The supported codecs are:

-   libavcodec: This codec package is capable of decoding
    H263/MJPEG/RV10/DivX3/DivX4/DivX5/MP41/ MP42/WMV1/WMV2/SVQ1/SVQ3
    encoded video streams and WMA (Windows Media Audio) v1/v2 audio. It
    is also known to be the fastest for this task.
-   Win32 codecs:
-   QuickTime codecs
-   XviD
-   XAnim: are the best codecs (full screen, hardware YUV zoom)
    fordecoding 3ivx and Indeo 3/4/5 movies

**gmplayer** is MPlayer with a graphical user interface;

{{< iref "#smplayer" "SMPlayer" >}} (GPL) is a GUI for mplayer or {{< iref "#mpv" "mpv" >}}.

{{< iref "video_edit#mencoder" "mencoder" >}}
is the encoder included in the mplayer distribution.

**References:**

-   [MPlayer Home page](http://www.MPlayerHQ.hu/),
-   [Mplayer documentation](http://www.mplayerhq.hu/DOCS/HTML/en/),
-   [MPlayer Features](http://www.mplayerhq.hu/design7/info.html).
-   [mplayer(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=mplayer(1))
-   Wikipedia {{< wp "MPlayer" >}}
-   [ArchWiki: Mplayer](https://wiki.archlinux.org/index.php/MPlayer)


## MPV {#mpv}

[mpv](https://mpv.io/) is a media player based on MPlayer and MPlayer2.

_MPlayer2_ was a fork of mplayer, that  the internal gui
_gmplayer_ and the encoder _mencoder_; and use shared libratries
instead of embedding {{< iref "ffmpeg" "ffmpeg" >}}.
It is dead and replaced with mpv.

Mpv also drop _mencoder_, but replace it with internal
[encoding](https://mpv.io/manual/stable/#encoding) facilities.
There are numerous other
[differences of mpv with mplayer and mplayer2
](https://github.com/mpv-player/mpv/blob/master/DOCS/mplayer-changes.rst).

-   [mpv source (GitHub)](https://github.com/mpv-player/mpv)
-   [mpv manual](https://mpv.io/manual/stable/),
    [FAQ](https://github.com/mpv-player/mpv/wiki/FAQ) and
    [Wiki](https://github.com/mpv-player/mpv/wiki).
-   Wikipedia: {{< wp "Mpv_(media_player)"  "MPV" >}}
-   [Archwiki -  Mpv](https://wiki.archlinux.org/index.php/Mpv)
-   [Gentoo Wiki - mpv](https://wiki.gentoo.org/wiki/Mpv)

There is a Debian package _mpv_, but mpv developpers
[recommand to use a newer version](https://mpv.io/installation/)
in deb-multimedia.

### MPV frontends

mpv itself has only a rudimentary {{< iref "#mpv_pseudo" "pseudo-gui" >}}
and many
[third party frontends
](https://github.com/mpv-player/mpv/wiki/Applications-using-mpv#gui-frontends)
see also the [list on Wikipedia
](https://en.wikipedia.org/wiki/Mpv_(media_player)#Interface_and_graphical_front-ends).

<a name="smplayer"></a>[SMPlayer](http://www.smplayer.info/)
(GPL) is a GUI for {{< iref "#mplayer" "mplayer" >}} or mpv
written in C++ with Qt4/Qt5. It supports [numerous formats and codecs
](http://www.smplayer.info/en/supported-formats-and-codecs), it can
play YouTube videos. And support [chromecast
](https://blog.smplayer.info/category/chromecast/) since v17.1
this need you have Chrome or Chromium installed. SMPlayer is in Debian.
-   [SMPlayer Blog](https://blog.smplayer.info/)
-   [Wikipedia: SMPlayer](https://en.wikipedia.org/wiki/SMPlayer).

[gnome-mpv/gnome-mpv](https://github.com/gnome-mpv/gnome-mpv) (GPL)
is a  GTK+ frontend for mpv.

<a name="mpv_pseudo-gui"></a>
It now provides a _pseudo-gui mode_ that you get by starting it
with:

    $ mpv  --player-operation-mode=pseudo-gui

or by using the `mpv.desktop` file



## [Sayonara](https://sayonara-player.com/index.php)
_Sayonara_ is a small C++/QT music player,
there is a [PPA repository for Sayonara
](https://launchpad.net/~lucioc/+archive/ubuntu/sayonara).
with i386 and amd64 packages.

On amd64 _Sayonara_ consume 68M res / 51M shr for _Sayonara
1.0.0 in may 2018.

## Totem {#totem}

[Totem](http://en.wikipedia.org/wiki/Totem_(media_player)) (GPL)
is a media player (audio and video) for GNOME based on xine-lib or
{{< iref "streaming#gstreamer" "GStreamer" >}}. Totem is able to play
all mainstream media formats supported by one of the two backends. It
also understands numerous playlist formats, including SHOUTcast, M3U,
XML Shareable Playlist Format (XSPF), SMIL, Windows Media Player
playlists and RealAudio playlists.

While Totem offers a gnome desktop integration, it's gnome
dependencies are moderate, wich allow to install it in lighter GTK
environments.

On an Amd64 in may 2018 Totem take 82M res / 46shr for a single ogg
track; 116M res / 57M shr for a tv broadcast on DLNA.

-   [Totem -  Gnome Home](http://www.gnome.org/projects/totem/)

## VideoLAN {#vlc}

[VideoLAN](http://www.videolan.org/) (GPL) targets streaming of MPEG-1,
MPEG-2,MPEG-4 and DivX files, DVDs, digital satellite and terrestial
television channels, and live videos on IP network

[VLC](http://www.videolan.org/vlc/) media player is a cross-platform
media player, and streamin server. Supported video formats and streaming
protocols are given in the [VLC features list
](http://www.videolan.org/vlc/features.html)

Since version 3.0.1 VLC support {{< iref "streaming#chromecast" "Chromecast" >}}.

**Refs:**

-   {{< wp "Wikipedia VLC media player" >}}
-   videolan.org documentation: [VLC Play-Howto (en)
    ](http://www.videolan.org/doc/play-howto/en/play-howto-en.html) (
    [french
    ](http://www.videolan.org/doc/play-howto/fr/play-howto-fr.html)),
-   [VLC Streaming-Howto (en)
    ](http://www.videolan.org/doc/streaming-howto/en/streaming-howto-en.html)
    ([french
    ](http://www.videolan.org/doc/streaming-howto/fr/streaming-howto-fr.html))
-   Actual documentation: is on
    [VideoLan Wiki](https://wiki.videolan.org/)
-   [VLC Streaming-Howto
    ](https://wiki.videolan.org/Documentation:Streaming_HowTo),
    [HowTo/Receive and Save a Stream - VideoLAN Wiki
    ](https://wiki.videolan.org/Documentation:Streaming_HowTo/Receive_and_Save_a_Stream/)
-   [ArchWiki - VLC
    ](https://wiki.archlinux.org/index.php/VLC_media_player)

## [Xine](http://www.xine-project.org/)
Xine (GPL) is a free multimedia player which plays back CDs, DVDs, and
VCDs, decodes AVI, MOV, WMV, and MP3 from local disk drives, and
displays multimedia streamed over the Internet.

Refs:
[Xine FAQ](http://xinehq.de/index.php/faq),
[Xine HowTo](http://dvd.sourceforge.net/xine-howto/),
[xine(1)
](http://manpages.debian.org/cgi-bin/man.cgi?query=xine(1)),
[aaxine(1)](http://man.cx/aaxine(1)),
[xine-remote(1)
](http://manpages.debian.org/cgi-bin/man.cgi?query=xine-remote(1)).


#[MPRIS](http://specifications.freedesktop.org/mpris-spec/latest/){#mpris}

The Media Player Remote Interfacing Specification is a standard D-Bus
interface which aims to provide a common programmatic API for
controlling media players.

The players supporting MPRIS include
{{< iref "#audacious" "Audacious" >}},
{{< iref "#clementine" "Clementine" >}},
, Dragon Player,
{{< iref "#exaile" "Exaile" >}},
{{< iref "#guayadeque" "Guayadeque" >}},
{{< iref "#bmpx" "BMPx" >}},
{{< iref "streaming#mopidy" "Mopidy" >}} with mopidy-mpris,
{{< iref "#mpd" "MPD" >}} via
{{< iref "#mpdris2" "mpDris2" >}},
{{< iref "#mpv" "mpv" >}} with the help of
[lua-mpris](https://github.com/dodo/lua-mpris#mpv),
{{< iref "#qmmp" "Qmmp" >}},
Songbird via a plugin,
{{< iref "#vlc" "VLC" >}} when launched with
`vlc --control dbus`,
{{< iref "#xmms2" "Xmms2" >}} via xmms2-mpris-bridge.

This
[shell script](https://gist.github.com/exic/1d051e3a15f61e06caf4), is
an example of MPRIS control of a player.

Other control tools are:

[playerctl](https://github.com/acrisci/playerctl)
:   is an mpris command-line controller and library for spotify.

[mpris-remote](http://incise.org/mpris-remote.html)
:   is a utility that controls an MPRIS-capable music player.
    [GitHub: mpris-remote](http://github.com/mackstann/mpris-remote/).
    mpris-remote is in debian.

# Mixers
[aumix](http://jpj.net/~trevor/aumix.html)
:   Aumix is a tty-based, interactive method of controlling a sound card
    mixer. It lets you adjust the input levels from the CD, microphone,
    and board synthesizers, as well as the output volume. Aumix can
    adjust audio mixers from the command line, from a script, or
    interactively at the console or terminal with an ncurses-based
    interface, or with a X11 interface named **aumix-X11**.

amixer, alsamixer from {{< iref "sound_libs#alsa" "alsa" >}} utilities.
:   amixer is the alsa text based mixer

    refs: [amixer(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=amixer(1))

:   alsamixer is a curse text mixer tool.

    refs:  [alsamixer(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=alsamixer(1))

[SDL\_mixer](http://www.libsdl.org/projects/SDL_mixer/)
:   A simple multi-channel audio mixer for SDL. It supports 4 channels
    of 16 bit stereo audio, plus a single channel of music, mixed by
    {{< iref "#item_mikmod" "MikMod" >}} MOD, Timidity MIDI and SMPEG MP3 libraries.
    The command line utilities are **playmus** and **playwave**
:   [SDL Mixer documentation
    ](http://jonatkins.org/SDL_mixer/SDL_mixer.html)

# Media centers and distributions {#media_centers}

[freevo](http://freevo.sourceforge.net/)
:   A linux distribution for multimedia either on a standalone PVR
    computer with a TV+remote, as well as on a regular desktop computer
    using the monitor and keyboard. Freevo is developped using the
    Python Language.

    -   [Freevo Wiki](http://freevo.sourceforge.net/cgi-bin/doc)


[geexbox](http://www.geexbox.org/en/index.html)
:   is a live cd distribution aimed at media playing. GeeXboX runs on
    x86, PowerPC and ARM devices.


<a name="mythtv"></a>[MythTV](http://www.mythtv.org/) (GPLv2)
:   _MythTV_ is a digital video recorder. Through a plugins system it
    can record and play back scheduled programs, schedule recordings
    automatically in advance, play external video, show photos, play
    music files, use your TV and a web camera as a video-telephone over
    the Internet, retrieve weather forecasts, and many other functions.

    -       [MythTV main page](http://www.mythtv.org/)
    -       [MythTV HowTo](http://www.mythtv.org/wiki/MythTV-HOWTO)
    -       [MythTV User Manual](http://www.mythtv.org/wiki/User_Manual:Index)
    -       [MythTV UPnP](http://www.mythtv.org/wiki/UPnP):
             MythTV has a built-in UPnP server.
    -       [ArchWiki: MythTV](https://wiki.archlinux.org/index.php/MythTV)
    -       Wikipedia: {{< wp "MythTV" >}}

    In 2018 no prepackged _MythTV_ exists for Debian you have to build
    your package from the source as described in
    [Installing MythTV on Debian
    ](https://www.mythtv.org/wiki/Installing_MythTV_on_Debian).

[rockbox](http://www.rockbox.org/)
:   is an open source replacement firmware for mp3 players. It runs on
    some models from Apple ipod, Archos, Cowon iaudio,Ipod, Iriver,
    MPIO, Olympus, Philips, Samsung, Sandisk, Sony, Toshiba.  _a
    release in 2017_

## Kodi {#kodi}
<a name="xbmc"></a>{{< wp "Kodi" >}} Kodi (formerly XBMC) (GPL)
is a cross-platform digital media hub and HTPC (Home theater PC)
software designed to be a    media player for the living-room TV.<br />

-   [Kodi Home](http://kodi.tv)
-   [Kodi Wiki](http://kodi.wiki/)
    -   [List of Kodi Devices
        ](https://kodi.wiki/view/Devices)
    -   [Raspberry Pi](https://kodi.wiki/view/Raspberry_Pi)
    -   [XBMC built-in UPnP A/V media server](http://kodi.wiki/view/UPnP/Server)
    -   [Kodi UPnP client](https://kodi.wiki/view/UPnP/Client)
    -   [Kodi as UPnP Control Point
        ](https://kodi.wiki/view/UPnP/Client#Sending_video_to_other_UPnP_targets).
    -   [PulseAudio](https://kodi.wiki/view/PulseAudio)
        s used when Kodi is installed in a desktop-environment rather than a
        dedicated/direct boot setup. PulseAudio allows normal video & audio playback in
        XBMC while at the same time allowing the user to get audio in their browser or
        other applications.
    -   [NFO FIles](https://kodi.wiki/view/NFO_files) can be used to provide metadata to
        the library for video and a music files.
    -   [Cue sheets](https://kodi.wiki/view/Cue_sheets)
    -   [UPnP server]](http://kodi.wiki/view/UPnP/Server).
    -   [List of built-in functions](https://kodi.wiki/view/List_of_built-in_functions).
    -   [External players](https://kodi.wiki/view/External_players)
-   [List of software based on Kodi - Wikipedia
    ](https://en.wikipedia.org/wiki/List_of_software_based_on_Kodi_and_XBMC).
-   [ArchWiki: Kodi](https://wiki.archlinux.org/index.php/Kodi)

On amd64 I have experienced Kodi playing a TV stream taking
98M res / 46M shr in may 2018 for kodi 2:17.6.

On raspberry PI 1 osmc distribution I have Kodi multiple threads
109M / 55 M shared.

-   `kodi-send`  is used for sending actions to a kodi server in the lan.
    It is in the Debian Package _kodi-eventclients-kodi-send_; Of course you don't need
    to have a kodi server on the machine where you install `kodi-send`. The
    actions you can send are listed in the [List of built-in functions
    ](https://kodi.wiki/view/List_of_built-in_functions)
-   There are many Firefox plugins to send content to Kodi, among them:
    [Send to Kodi](https://addons.mozilla.org/en-US/firefox/addon/send-to-xbmc-kodi/)
    ( [GitHub Repository](https://github.com/dirkjanm/firefox-send-to-xbmc)) and its
    fork [send to Kodi2](https://addons.mozilla.org/en-US/firefox/addon/send-to-kodi-2/)
    (  [GitHub Repository](https://github.com/WPettersson/firefox-send-to-xbmc))
    [kodi-control](https://addons.mozilla.org/en-US/firefox/addon/kodi-control/)
    ( [GitHub Repository](https://github.com/LendoK/kodi-control)),
    [Play to Kodi](https://addons.mozilla.org/en-US/firefox/addon/play-to-kodi4/)
    ( [GitHub Repository](https://github.com/maciex/play-to-kodi) with numerous forks
    and a [Chrome Version](https://chrome.google.com/webstore/detail/play-to-kodi/)),
    [goldenratio/xbmc-web-remote](https://github.com/goldenratio/xbmc-web-remote) can be
    used with Firefox, Chrome or Opera,
-   [send2kodi](http://kodi.dnmx.ch/) is a javascript page to send an url to kodi
    Fabio Rämi (dnmx)
    [describes it in his blog](https://dnmx.ch/blog/2016/03/send2kodi.html).
-   There are also some shell scripts to send an url to kodi
    [allejok96/send-to-kodi](https://github.com/allejok96/send-to-kodi/),
    [facmachado/send2kodi](https://github.com/facmachado/send2kodi/),
    [nawar/kodi-cli](https://github.com/nawar/kodi-cli) and its fork
    [/WPettersson/kodi-cli](https://github.com/WPettersson/kodi-cli).
-   [osmc](https://osmc.tv/) is a distribution of Kodi based on Debian.
    All resources are on the [OSMC Wiki](https://osmc.tv/wiki/).
    It can be installed on Raspberry Pi, Apple TV first generation, and a their own
    platform [Vero](https://osmc.tv/vero/), an ARM64 platform with 2G DDR3, USB2, Gigabit
    ethernet, IR and RF receiver, with a price ~ 100€.
    -   [Github - osmc](https://github.com/osmc/osmc)

-   [xbev](https://github.com/bobo1on1/xbev/wiki) (GPL)
    is a simple desktop eventclient for Kodi, written in Python, it creates a window on
    using gtk and sends any keypresses received on that window to Kodi's eventserver.
-   [MediaElch](https://www.kvibes.de/mediaelch/) (LGPL)
    ([GitHub Repository](https://github.com/komet/mediaelch)) is a MediaManager for Kodi,
    which manage the ``nfo`` files used by Kodi. It is a C++ application, an appimage is
    provided (no package).

<!--  Local Variables: -->
<!--  ispell-local-dictionary: "english" -->
<!--  mode: markdown -->
<!--  End: -->
