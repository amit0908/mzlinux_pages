---
title: Web Feed
---


# Feed Formats {#rss_formats}
A {{< wp "Web feed" >}}, or _News Feed_  is a document (often XML-based) which include
web links to Web content.

-   The main formats for syndication, used to exchange lists of feeds between feed
    aggregators, are
    {{< wp "RSS" >}},
    {{< wp "JSON Feed" >}},
    {{< wp "OPML" >}}  is an XML format for outlines,
    {{< wp "Atom_(Web_standard)"  "Atom" >}},
    the last article includes a [comparison between RSS 2.0 and Atom
    ](https://en.wikipedia.org/wiki/Atom_(Web_standard)#Atom_compared_to_RSS_2.0).
-   [RSS 2.0 Specification](http://blogs.law.harvard.edu/tech/rss)
-   [RSS Tutorial](http://www.mnot.net/rss/tutorial/)
    by Mark Nottingham.
-   [rfc4287 The Atom Syndication Format](https://tools.ietf.org/html/rfc4287).
-   [Podcast](http://en.wikipedia.org/wiki/Podcast)
    are syndication feeds embedding digital media files.
-   [CreativeCommons.org: Podcasting legal guide](http://wiki.creativecommons.org/Podcasting_Legal_Guide).
-   [Wikibooks: Podcasting](http://en.wikibooks.org/wiki/Podcasting)
    is a short podcast publication tutorial.
-   [Apple Podcasting and iTunes Technical Specification
    ](http://www.apple.com/itunes/store/podcaststechspecs.html)
    give the format used by the apple itunes software.
-   [FeedValidator](http://feedvalidator.org/)
    (MIT license) is a rss-2.0 and atom-1.0 online validator.


# Feed readers
-   {{< wp "News Aggregator" >}} are  client software to read syndicated contents.
-   Wikipedia {{< wp "News Aggregator" >}}, {{< wp "Comparison of feed aggregators" >}},
    [w:List of feed aggregators.

## Online {#online_aggregator}
[Google Reader](http://www.google.com/reader/)
was a popular an online RSS aggregator closed by Google at
begining of July 2013. It can be replaced by  many other
[free or open source online rss readers
](http://alternativeto.net/software/google-reader/?license=free&platform=online)

{{< wp "Firefox" >}} can read RSS or atom flux with the {{< wp "Live bookmarks" >}}
feature. It does not have all all the features of an aggregator, but could be an easy
way to always access your feeds.

-   [CommaFeed](https://github.com/Athou/commafeed)
    <a name="commafeed"></a> (Apache License)
    is a Google Reader inspired self-hosted RSS reader. It has quite heavy
    java requirements, but there is a free online server at
    [commafeed.com](https://www.commafeed.com/welcome).
    -   Commafeed has a public [REST API](https://www.commafeed.com/api/)
    -   There many android applicationss
        the official one is [commafeed extension for News+
        ](https://play.google.com/store/apps/details?id=com.commafeed.newspluscommafeedreader)
        (697K) + [News+](https://play.google.com/store/apps/details?id=com.noinnion.android.newsplus).

-    <a name="feedly"></a>{{< wp "Feedly" >}}
    is an online news aggregator. It is the most popular
    since Google close down Google Reader.
    [Feedly website](https://feedly.com/).
    -   [feedly public API](https://developer.feedly.com/)
    -   Feedly has {{< wp "OPML" >}} support as explained in the
        [feedlyBlog page: New OPML Import](https://blog.feedly.com/opml/).
        You can export your feeds as OPML by accessing <https://feedly.com/i/opml>,
        and import them with the +Add Content button at the bottom left of the Feedly
        app or by visiting <https://feedly.com/i/cortex>.

        There is also an [OPML API](https://developer.feedly.com/v3/opml/).
    -   There is an [official android application
        ](https://play.google.com/store/apps/details?id=com.devhd.feedly)
        quite big ~10MB.

        If you try to access internet from android for some reason, feedly redirect your
        browser to the application download page as soon it detect an android client,
        rendering impossible to access to the site without changing the user-agent.

    -   The unofficial android application [FeedMe
        ](https://play.google.com/store/apps/details?id=com.seazon.feedme)
        allows also to access Feedly, It is a light 1.7M application.
    -   Feedly allow to [save articles on reading apps
        ](https://blog.feedly.com/seven-ways-to-save-articles-that-you-read-in-feedly/)
        Instapaper, Evernote, OneNote, Pocket, and Dropbox.
    -   We can use {{< wp "IFTTT" >}} to automatically send saved stories.
-   [Leed](http://leed.idleman.fr/) (License Creative common by nc-sa),
    [GitHub repository](https://github.com/ldleman/Leed)
      is a web-based news reader, it needs PHP with MySQL, and has an android application.
-   [Miniflux](https://github.com/fguillot/miniflux) (AGPL)
    is a web-based news reader, it needs PHP with sqlite and XML extensions.
    It does not use social network, and does not allow advertisements or pixel tracking.
    -   [The hosted version of Miniflux
        ](http://miniflux.net/hosted.html) is proposed for a a one-time fee of 15€
-   [NewsBlur](http://www.newsblur.com/) <a name="newsblur"></a> (MIT)
    is an open source web newsreader,
    [GitHub: NewsBlur](https://github.com/samuelclay/NewsBlur)
    is a python/django application needing mysql/postgresql and
    MongoDB.{{< wp "NewsBlur"  "Wikipedia: NewsBlur" >}}.<br>
    The [NewsBlur hosted newsreader](http://www.newsblur.com/) allow
    free access limited to 64 sites. There is a free android
    application for android > 3.0 and some unofficial ones.
    It can also be synchronized with
    {{< iref "#newsboat" "NewsBoat" >}}.
-   [Tiny Tiny RSS](http://tt-rss.org/redmine/projects/tt-rss/wiki) (GPL)
    <a name="tinytinyrss"></a>
    is a web-based  PHP and Ajax news feed (RSS/Atom) reader and
    aggregator it can replace Google Reader. It is in debian
    -   On the server side tt-rss needs an httpd server with PHP with many libraries,
        some javascript libraries including dojo,
        and a sql databse PostgreSQL or MySQL.
    -   On The client side you need _Chrom(e/ium)_ or _Firefox_.
    -   Tiny Tiny RSS has many
        [plugins](http://tt-rss.org/redmine/projects/tt-rss/wiki/Plugins)
    -   The [Android Client
         ](http://tt-rss.org/redmine/projects/tt-rss-android/wiki)
        _(1.1M)- is [on google store
        ](https://play.google.com/store/apps/details?id=org.fox.ttrss)
    -   [ttrss-mobile](https://github.com/mboinet/ttrss-mobile)
        is a Jquery-mobile webapp for Tiny Tiny RSS using Backbone.js and
        RequireJS.
    -   A [Tiny Tiny RSS Demo is available at softaculous
        ](http://www.softaculous.com/demos/Tiny_Tiny_RSS)
-   [selfoss](http://selfoss.aditu.de/) (GPL)
    a self hosted web reader, need an httpd server, PHP and
    one of MySQL, PostgreSQL or Sqlite. IT has a
    [Restful API for Apps or any other external access
    ](https://github.com/SSilence/selfoss/wiki/Restful-API-for-Apps-or-any-other-external-access),
    and an [Android Client
    ](https://play.google.com/store/apps/details?id=fr.ydelouis.selfoss)

Among other free online RSS readers, that I have not tested:
[InoReader](https://inoreader.com/), [EldonReader](http://reader.eldonlabs.com),
[G2Reader](http://www.g2reader.com/fr/), [Go Read](http://www.goread.io),
[HiveReader](http://hivereader.com), [SilverReader](http://silverreader.com),
[The Old Reader](https://theoldreader.com/).


## Desktop {#desktop_aggregator}
_I mention only some light rss readers, a lot of desktop integrated
readers are depending of a full kde or gnome installation,
and I never had the opportunity to use them.

-   {{< wp "Canto_(news_aggregator)"  "Canto" >}} - [Canto Home](http://codezen.org/canto/) (GPL)
    is a terminal based aggregator for online news written in python,
    it is packaged in all main distributions.<br />
    The new version is [Canto-ng](http://codezen.org/canto-ng/).
    _not yet packaged in Debian_
-   [Liferea](http://liferea.sourceforge.net/) (GPL) an  aggregator written in C + GTK2.
    It synchronizes with TheOldReader  and with {{< iref "#tinytinyrss" "TinyTinyRSS" >}},
    [Inoreader](http://www.inoreader.com/), [Reedah](https://www.reedah.com/)
-    <a name="newsboat"></a>[newsboat](https://github.com/newsboat/newsboat) (MIT)
    is an actively maintained fork of [newsbeuter](http://www.newsbeuter.org/) which was
    abandonned in 2017.
    <a name="newsbeuter"></a>.
    It is a text mode rss feed reader with podcast support written in Rust (newsbeuter
    was written in C++) with ncurses UI. _packaged in Debian._
    -   [NewsBoat Home](https://newsboat.org/) with link to the latest documentation.
    -   _NewsBoat_ can synchronize with _The Old Reader_,
        {{< iref "#newsblur" "NewsBlur" >}},  {{< iref "#tinytinyrss" "TinyTinyRss" >}},
        _FeedHQ_, _Bazqux_, _ownCloud News_ and _nextCloud News_,
        _Inoreader_
    -   _NewsBoat_ can export and import OPML, and have a one way synchronisation
        with any service that publishes your subscriptions in OPML format.
        _NewsBoat knows what what you have read on the remote, but the remote ignore
        what you have read on NewsBoat_
-   <a name="newsticker"></a>
    [NewsTicker](http://www.emacswiki.org/emacs/NewsTicker) (GPL)
    is an rss/atom reader for emacs.
-   [Nuush](http://chr.tx0.org/nuush) ([unlicense](http://unlicense.org/))
    is a bash command line rss reader it uses the
    [XmlStarlet](http://xmlstar.sourceforge.net/) xml command line utilities.
    Xmlstarlet is packaged in Debian, but not Nuuch.
-   [Rawdog](http://offog.org/code/rawdog.html "offog.org rawdog")
    is a RSS Aggregator written in Python using
    [feedparser](http://www.feedparser.org/), that reads articles from a
    number of feeds and writes out a single HTML file. _It is in debian_
-   [rsstail](http://www.vanheusden.com/rsstail/) (GPL)
    monitors an rss-feed and if it detects a new entry it'll emit only
    that new entry. _It is in debian._
    -   [rsstail GitHub repository](https://github.com/flok99/rsstail)

-   [Snownews](http://kiza.kcore.de/software/snownews/)
    is a text mode RSS/RDF newsreader. It depends on ncurses
    for the user interface and uses libxml2 for XML parsing.
    A [Snownews deb package
    ](http://packages.debian.org/search?keywords=snownews)
    is available.


# Podcasters.
-   [BashPodder](https://github.com/funnelfiasco/bashpodder)
    a simple bash podcast downloader, it requires bash, wget
    or curl, sed and xsltproc.
-   [MashPodder](https://github.com/chessgriffin/mashpodder)
    is a podcatching client based on BashPodder.

# Rss converter/generator

-   [JabRSS](http://dev.cmeerw.org/jabrss/Documentation) (GPL)
    is a simple RSS (RDF Site Summary) headline notification service for Jabber.
-   [RssCalendar](http://www.rsscalendar.com/)
    is a free web service that
    creates RSS feeds that show  calendars by day, week, month, or
    year.
-   [rss2email](https://pypi.python.org/pypi/rss2email/)
    is a python gateway from rss to email. It is in pypi and packaged
    for Debian and Ubuntu. _2011_
    -   [rss2email GitHub repository](https://github.com/wking/rss2email).
-   [rss2jabber](http://sourceforge.net/projects/rss2jabber.berlios/)
    is a PHP, MySQL application that gathers articles from RDF/RSS/Atom
    feeds and sends them to an IM client.
    It is available at `rss2jabber@jabber.fr`.
-   [Talkfeed](http://code.google.com/p/talkfeed/) (Apache License)
    is a tool to receive new posts from RSS and Atom feeds
    directly in your Jabber client.
    The application is
    [hosted on Google App Engine](http://talkfeed.appspot.com)


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
