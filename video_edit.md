<!--
.. description:
.. date: 2015-04-12
.. slug: video_edit
.. tags:
.. link:
.. book: mzlinux
.. title: Video Encoders / Editors
-->

[TOC]

The main utility
[ffmpeg alias libav](/node/ffmpeg "internal reference")
has its own page.

# Guides

-   [DVD-HOWTO](http://en.tldp.org/HOWTO/DVD-HOWTO.html) provides
    step by step instructions on getting DVD movies to play in Linux. _2000_
-   The new Gentoo Wiki:
    [MPlayer](http://wiki.gentoo.org/wiki/MPlayer),
    [CD/DVD/BD Writing](http://wiki.gentoo.org/wiki/CD/DVD/BD_Writing),
-   [DVD Frequently Asked Questions](http://dvddemystified.com/dvdfaq.html) _(uptodate 2013)_
-   [ArchWiki: Convert any Movie to DVD Video
    ](https://wiki.archlinux.org/index.php/Convert_any_Movie_to_DVD_Video)

# [Mencoder](http://www.mplayerhq.hu/) (GPL) {#mencoder}

**mencoder** is a simple movie encoder, associated with
[Mplayer](/node/media_players#mplayer "internal reference") and designed to encode
MPlayer-playable movies. It encodes to DivX4, XviD, one of the
libavcodec codecs and PCM/:MP3/:VBRMP3 audio in 1, 2 or 3 passes.

**Refs:**

-   [Mplayer Home Page](http://www.mplayerhq.hu/design7/info.html),
-   [Basic usage of MEncoder
    ](http://www.mplayerhq.hu/DOCS/HTML/en/mencoder.html)
-   [Encoding with MEncoder
    ](http://www.mplayerhq.hu/DOCS/HTML/en/encoding-guide.html)
    from
    [Mplayer Documentation](http://www.mplayerhq.hu/DOCS/HTML/en/).
-   [MEncoder - ArchWiki
    ](https://wiki.archlinux.org/index.php/MEncoder)
-   [HOWTO Convert video files](http://en.linuxreviews.org/HOWTO_Convert_video_files)
    using mencoder.

# [w:OggConvert]  {#oggconvert}

__0ggconvert__ (LGPL) convert audio and video files of various types
into Ogg Vorbis audio format, and the Theora, VP8 and Dirac video
formats. It supports Ogg, Matroska and WebM containers for
output. __0ggconvert__ is written in Python - GTK+ and depends only on
the GStreamer framework

# [PiTiVi](http://www.pitivi.org/) {#pitivi}

__PiTivi__ (LGPL) is an audio/video editing software written in python
GTK+ that uses the gstreamer framework.
Wikipedia: [w:PiTiVi].

# Other tools
_some of these are older_

[Avidemux](http://avidemux.sourceforge.net/) (GPL)
:   [Avidemux](http://avidemux.sourceforge.net/)
    is a video editing and encoding tool. It can encode video
    in the following codecs: dvd, FFV1, H.263, H.264, x264, HuffYUV,
    MJPEG, MJPEG-4, Snow, SVCD, VCD, XVCD, Xvid. For audio the
    following codecs are available: mp3 (with lame), vorbis (with
    libvorbis), AAC (with FAAC), MP2 and AC-3 (with libavcodecs), MP2
    (with TwoLame), WAV PCM and WAV LPCM. The documentation is in the
    [Avidemux wiki](http://www.avidemux.org/admWiki/index.php).

    It is not in Debian but in deb-multimedia.

[dvdauthor](http://dvdauthor.sourceforge.net/) (GPL)
:   `dvdauthor` is simple set of tools to help author a DVD. The idea
    is to be able to create menus, buttons, chapters, etc. It is
    packaged in Debian.

    [tutorial on dvdauthor](http://gecius.de/linux/dvd.html) by Jens
    Gecius

    [qdvdauthor](http://qdvdauthor.sourceforge.net/) is a frontend for
    _dvdauthor_

    [GitHub: dvdauthor](https://github.com/ldo/dvdauthor)

[Transcode](https://bitbucket.org/france/transcode-tcforge)
:   _Transcode_ is a  text-console utility for video stream processing.
    It can import of MPEG-1/2, Digital Video, and other formats
    and write to AVI files with DivX, OpenDivX, XviD, Digital Video or other codecs.

    Except some minor maintenance the development stopped in 2008. It
    is packaged in Debian.

[vcdimager](http://www.gnu.org/software/vcdimager/) (GPL)
:   VCDImager is a full-featured mastering suite for Video CD's and
    Super Video CD's. _Old tool main developement from years 200O-2005
    but still packaged in Debian_

[vobcopy](http://vobcopy.org/) (LGPL)
:   _vobcopy_ copy (and decrypt) vob files. The development stopped in 2008.


# Encoding Frontends

[acidrip](http://untrepid.com/acidrip/ "untrepid.com acidrip") (GPL)
:   _aciprip_ is a Gtk2::Perl frontend for mencoder and mplayer. It
    has an introductory
    [article in linux
    journal](http://www.linuxjournal.com/article/9124)

[dvd::rip](http://www.exit1.org/dvdrip/)
:   _dvd::rip_ is a Perl Gtk+ based DVD copy program built on top of
    [Transcode](#transcode)

[HandBrake](https://handbrake.fr/)
:   is a tool for converting video from nearly any format to a
    selection of modern, widely supported codecs.
    _In Debian and deb-multimedia_

[iso2mkv](http://5ko.free.fr/en/iso2mkv.html) (MIT license)
:   _iso2mkv_ is a bash script based on mplayer, mencoder, oggenc
    or lame, and mkvmerge for automated DVD to XviD/vorbis MKV video
    conversion.

[lives](http://lives.sourceforge.net/)  (GPL)
:   _LiVES_ is a Video Editing System that use mplayer, imagemagick,
    perl and gtk+

[lxdvdrip](http://sourceforge.net/projects/lxdvdrip/) (GPL)
:   _lxdvdrip_ is a command line tool to rip and burn a video DVD. It uses
    [mencoder](#mencode), [transcode](#transcode),`dvdbackup`

[ogmrip](http://ogmrip.sourceforge.net/) (LGPL)
:   _ogmrip_ is an application and a set of libraries for ripping
    and encoding DVD into AVI, OGM MP4 or Matroska files using a wide
    variety of codecs (vorbis, mp3, pcm, ac3, dts, aac, xvid, lavc,
    x264, theora). OgmRip relies on mplayer, mencoder, ogmtools,
    mkvtoolnix, mp4box, oggenc, lame, and faac to perform its tasks.
    There is a CLI client, it's called shRip. _In Debian and deb-multimedia._

[TEncoder](http://tencoder.sourceforge.net/)
:   is a multithreaded video and audio converter that uses MEncoder,
    MPlayer and FFMpeg. It uses
    [youtube-dl](#youtube-dl "internal reference") to download
    video/audio from video sites like youtube.  It can also rip
    unprotected DVDs. It can convert video and audio type to each
    other.  Subtitles with same name as video can be hard-coded into
    video.

[Thoggen](http://thoggen.net/) (GPL) <a name="thoggen"></a>
:   _Thoggen_ is a DVD backup utility for Linux, based on GStreamer
    and Gtk+ which encodes into Ogg/Theora video. features: GUI,
    resizing, cropping, language Selection for audio track.
    _No longer in debian_

[VLC](/node/streaming#vlc)
:   _VLC_ can be used for transcoding videos as explained in the
    [VLC wiki: Transcode](https://wiki.videolan.org/Transcode/).

# SWF tools
[swftools (GPL)](http://www.swftools.org/)
:   SWF Tools is a collection of SWF manipulation and creation
    utilities. It can convert from jpeg, png, gif, pdf, avi, wav, ttf
    fonts to swf. It allows also to combine swf files and to extract
    sound, movies, data from swf. _active in 2013_

[w:Google Swiffy]
:   is a web-based tool developed by Google that converts SWF files to
    HTML5. Its main goal is to display Flash contents on devices that
    do not support Flash. You can upload your swf to
    [Swiffy](https://developers.google.com/swiffy/) and get a
    it converted to html5.

    -   [Swiffy Home](https://developers.google.com/swiffy/)

# Subtitles editors

-   [gaupol](https://github.com/otsaloma/gaupol) (GPL) is a gtk
    subtitle editor. Gaupol is in Debian.
-   [gnome-subtitle](http://gnome-subtitles.sourceforge.net/) is a
    subtitle editor for gnome, written in mono. It is in Debian.
-   [Sam Hocevar: DVD Subtitles](http://sam.zoy.org/doc/dvd/subtitles/)
    explains the subtitle stream

# Screencasting {#screencast}
-   Wikipedia [w:Screencast] and
    [w:Comparison of screencasting software]
-   [ArchWiki: list of screencasting software
    ](https://wiki.archlinux.org/index.php/List_of_applications/Multimedia#Screencast)
-   [xvidcap](http://xvidcap.sourceforge.net/)
    (GPL) is a screen recording utility using FFMPEG's
    libavcodec/libavformat. _2006_
-   [recordMyDesktop](http://recordmydesktop.sourceforge.net/)
    is a desktop session recorder it records theora video with
    ogg vorbis audio. recordMyDesktop has a gtk and a qt frontend.
    -   [Screencasts in Ubuntu, part 1: recordmydesktop
        ](http://polishlinux.org/linux/ubuntu/screencasts-in-ubuntu-part-1/)
        by Marcin Seredyński is a recordmydesktop tutorial.
-   [istanbul](https://wiki.gnome.org/Projects/Istanbul)
    (GPL) is a gnome project written in python. It is a desktop
    session recorder for the Free Desktop. It records your session
    into an Ogg Theora .
-   [vnc2swf](http://www.unixuser.org/~euske/python/vnc2flv/index.html)
    is a screen recorder either build in python
-   [ffmpeg](/node/ffmpeg "internal reference") or
    [libav](/node/ffmpeg "internal reference")
    can be used for screencasting as described in
    [Screencasts in Ubuntu, part 2: FFmpeg
    ](http://polishlinux.org/linux/ubuntu/screencasts-in-ubuntu-part-2/)
    by Marcin Seredyński.

# Video download helpers {#video_download_helpers}
-   Wikipedia [w:Comparison of YouTube downloaders],
    they are also listed in
    [w:Comparison of download managers]

## scripts
-   [telecharger-streaming - Documentation Ubuntu Francophone
    ](http://doc.ubuntu-fr.org/telecharger_streaming)
-   [clive](http://clive.sourceforge.net/)
    written in perl _2012_ and it's c++ clone
    [cclive](http://cclive.sourceforge.net/) _2013_ are command line
    utilities for extracting videos from video sharing Web sites like
    YouTube. It can background and work while the user is
    not logged on.
-   <a name="youtube-dl"></a>[youtube-dl
    ](http://rg3.github.io/youtube-dl/)
    is a python (2 or 3) script to dowload videos from [many sites
    ](http://rg3.github.io/youtube-dl/supportedsites.html).
    Youtube-dl can use the following external downloaders: aria2c,
    avconv, axel, curl, ffmpeg, httpie, wget
    It is in debian.
    -   [GitHub: youtube-dl](https://github.com/rg3/youtube-dl)
-   [Pafy](http://pythonhosted.org/pafy/)
    is a Python library and cli to download YouTube content and
    retrieve metadata.  It is in the debian package _python-pafy_.
    -   [GitHub: pafy](https://github.com/mps-youtube/pafy)
-   [get-flash-videos](http://code.google.com/p/get-flash-videos/)
    a perl program to download videos from various Flash-based video
    hosting sites, without having to use the Flash player, which allow
    to download without having the last version of the player. It is
    in debian.
    -   [get-flash-videos GitHub repo
        ](https://github.com/monsieurvideo/get-flash-videos),
        [Nigel Taylor get-flash-video Github repo
        ](https://github.com/njtaylor/get-flash-videos/).
-   [Quvi](http://quvi.sourceforge.net/)
    contains a command line program to extract and download video
    files using libquvi, a library to parse Adobe flash video download
    links. It supports Youtube and other similar video websites. It
    provides access to functionality and data through an API, and does
    not enable or require the use of the flash technology. Quvi is in
    Debian.
    -   [ArchWiki - Quvi](https://wiki.archlinux.org/index.php/Quvi)
-   [StreamStudio](https://www.streamstudio.me/) (GPL)
    previously _Ht5streamer_ is an  application streaming, based on
    node-webkit and developed using web technologies such as HTML5,
    JavaScript and CSS. It allows you to view, download and transcode
    videos from Youtube, Dailymotion and supports plugins for other
    services like  t411, Cpasbien, Twitch, Kickass, OMG Torrent.
    -   [StreamStudio Forum](https://forum.streamstudio.me/)
        _en français_.

## browser extensions
-   [video bookmarlets
    ](http://1024k.de/bookmarklets/video-bookmarklets.html)
    to integrate with a javascript able browser
-   [w:Video DownloadHelper]  is an extension for Firefox  to
    download videos from sites that stream videos through HTTP, such as
    YouTube.   [Video DownloadHelper addon page
    ](https://addons.mozilla.org/fr/firefox/addon/video-downloadhelper/)
-   [YouTube Downloader for Android
    ](http://sourceforge.net/projects/ytdownloader/)
    download YouTube video and extract/convert audio to mp3. For
    Android4+

## Download sites
-   There are also dome download site to help the flv downloading:
    [Keepvid](http://keepvid.com/) and
    [DownloadFlv](http://www.downloadflv.com/)
-   The [Wikimedia Commons](http://commons.wikimedia.org/wiki/Main_Page)
    is a project that provides a central repository for free
    images, music, sound & video clips and, possibly, texts and spoken
    texts.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
