<!--
.. description:
.. date: 2015-12-22
.. slug: security
.. tags:
.. link:
.. book: mzlinux
.. title: Security
-->

[TOC]

See also the [Authentication section
](/node/authentication "internal reference"),

An important part of security is [Network security
](/node/network_security "internal reference").

# General references {#references}
-   Wikipedia: [w:Category:Computer security exploits]
-   [Security HOWTO](http://www.tldp.org/HOWTO/Security-HOWTO.html)
    is a guide for the linux administrator _2004_.
-   [Gentoo Security Handbook
    ](https://wiki.gentoo.org/wiki/Security_Handbook)
    teach how to harden different parts of your system to make it more
    secure.
-   [ArchWiki: Security](https://wiki.archlinux.org/index.php/security).
-   [ArchWiki: List of applications - Security
    ](https://wiki.archlinux.org/index.php/List_of_applications/Security).
-   [Computer and Network Security
    ](https://engineering.purdue.edu/kak/compsec/Lectures.html)
     a set of lectures by Avinash Kak with Python and Perl exercises.
-   [Security Engineering](http://www.cl.cam.ac.uk/~rja14/book.html)
    _2nd edition 2008_
    an online book by Bruce Schneier.
-   [linuxsecurity.com](http://linuxsecurity.com/),
    [linuxsecurity ressources](http://www.linuxsecurity.com/content/view/101892/155/)


## References en Français
-   [Agence Nationale de la Sécurité des Systemes d'Information
    (ANSSI)](http://www.ssi.gouv.fr/).
    -   [Index des Guides des Bonnes Pratiques
        ](http://www.ssi.gouv.fr/particulier/bonnes-pratiques/).
    -   [Recommandations pour la mise en place de cloisonnement
        système (pdf)
        ](http://www.ssi.gouv.fr/uploads/2017/12/guide_cloisonnement_systeme_anssi_pg_040_v1.pdf)
    -   [Administration sécurisée des systèmes d’information – v.2
        (pdf)
        ](http://www.ssi.gouv.fr/uploads/2015/02/guide_admin_securisee_si_anssi_pa_022_v2.pdf).
    -   [Recommandations de sécurité relatives à un système GNU/Linux
        (pdf)
        ](http://www.ssi.gouv.fr/uploads/IMG/pdf/NP_Linux_NoteTech_1_1.pdf).
    -   [Recommandations de sécurité relatives aux mots de passe (pdf)
        ](http://www.ssi.gouv.fr/uploads/IMG/pdf/NP_MDP_NoteTech.pdf).
-   [SecuObs L'observatoire de la Sécurité sur Internet
    ](http://www.secuobs.com/) _semble dormir depuis 2014_:
    [Tutoriels](http://www.secuobs.com/sommaires/Tutoriels.html)
-   [Direction des Systèmes d'Information Pôle ARESU
    ](https://aresu.dsi.cnrs.fr/IMG/pdf/certificats.kezako.pdf)
    : [Index des rubriques sur la sécurité
    ](https://aresu.dsi.cnrs.fr/spip.php?rubrique16)
-   [Certificats (électroniques) Pourquoi? Comment? (pdf)
    ](https://aresu.dsi.cnrs.fr/IMG/pdf/certificats.kezako.pdf)
    de Jean-Luc Archimbaud _2000_ est une présentation générale non
    technique de l'utilisation des certificats électroniques.
-   [Anne Canteaut](https://www.rocq.inria.fr/secret/Anne.Canteaut/)
    directrice de l'[Équipe Secret de l'INRIA
    ](https://www.inria.fr/equipes/secret) a quelqes articles de
    vulgarisation:
    -   [La cryptographie ou les mathématiques au service de la protection
        de l'information (pdf)
        ](http://www-rocq.inria.fr/secret/Anne.Canteaut/slides.pdf)
        une présentation élémentaire de la cryptographie dans un jeux
        de transparents destiné à des élèves de terminale.
    -   [La cryptologie moderne (pdf)
        ](http://www-rocq.inria.fr/secret/Anne.Canteaut/crypto_moderne.pdf)
        introduction à la cryptographie claire et accessible.
        transparents
    -   [Cryptanalyse des chiffrements à clef secrète par blocs (pdf)
        ](https://www.rocq.inria.fr/secret/Anne.Canteaut/Publications/Canteaut02a.pdf)
-   [Sécuriser son infrastructure avec GNU/Linux - partie 1
    ](https://www.supinfo.com/articles/single/7480-securiser-son-infrastructure-avec-gnu-linux-partie-1)
    et
    [Sécuriser son infrastructure avec GNU/Linux - partie 2
    ](https://www.supinfo.com/articles/single/7486-securiser-son-infrastructure-avec-gnu-linux-partie-2).

# Secure Programming
-   Wikipedia: [w:Security testing], [w:Buffer overflow],
    [w:Heap overflow], [w:Buffer overflow protection],
    [w:Dangling pointer].
-   [Secure Programming for Linux and Unix HOWTO
    ](http://www.dwheeler.com/secure-programs/Secure-Programs-HOWTO/index.html)
    by David A. Wheeler. provide a set of guidelines for writing secure
    programs for Linux. Specific sections for C, C++, Java, Perl, PHP,
    Python, Tcl, and Ada95 are included. _last release 2015_
-   [Practical Unix & Internet Security chapter 16: Secure
    Programming Techniques
    ](http://www.onlamp.com/pub/a/onlamp/excerpt/PUIS3_chap16/index1.html).
-   [Secure Programming for Linux and Unix HOWTO
    ](http://www.dwheeler.com/secure-programs/Secure-Programs-HOWTO/index.html)
    by David A. Wheeler has a section on C/C++ program security and a
    [chapter on how to avoid buffer overflow
    ](http://www.dwheeler.com/secure-programs/Secure-Programs-HOWTO/buffer-overflow.html).

## Program security testing tools
-   [bfbtester](http://bfbtester.sourceforge.net/)
    perform checks of  command line argument and environnement variable
    overflows; and unsafe tempfile names. It is an old program no
    longer developped since 2001, but is in Debian.
-   [flawfinder](http://www.dwheeler.com/flawfinder/) (GPL) is a
    program that examines source code and reports possible security
    weaknesses.
-   [PEframe](https://github.com/guelfoweb/peframe) (MIT License)
    is a python tool to perform static analysis on Portable Executable
    malware. It is in Debian.
-   [Splint](http://splint.org/) (GPL) is a tool for
    statically checking C programs for security vulnerabilities and
    coding mistakes.


# Cryptography
-   Wikipedia : [w:Public-key cryptography]
-   For a security guide look at
    [bettercrypto](https://bettercrypto.org/)
    The guide is [Applied Crypto Hardening (pdf)
    ](https://bettercrypto.org/static/applied-crypto-hardening.pdf).

    The source is
    [GitHub: BetterCrypto/Applied-Crypto-Hardening
    ](https://github.com/BetterCrypto/Applied-Crypto-Hardening)
    and you can also build the guide in html, test or markdown.
-   [Cours de Cryptographie](http://courscrypto.org/)
    by [Nadim Kobeissi](https://nadim.computer/) _look also to his
    blog at the same address.
-   [Crypto faq (pdf)](
    http://www.rsasecurity.com/rsalabs/faq/files/rsalabs_faq41.pdf
    from RSA Laboratories is an introduction to public key
    cryptography _outdated: 2000_.

    It has a section on
    _Patents on Cryptography_ which is a very convenient resource
    which can be deepened with the
    [Crypto Law Survey](http://www.cryptolaw.org/).
-   [Cryptography FAQ
    ](http://www.faqs.org/faqs/cryptography-faq/part1/)
    _outdated: 2000-2004
-   [Handbook of Applied Cryptography
    ](http://www.cacr.math.uwaterloo.ca/hac/index.html)
    by Alfred J. Menezes, Paul C. van Oorschot and Scott A. Vanstone
    _5th edition 2001_ CRC Press. Is available in pdf.
-   [Crypto Law Survey](http://www.cryptolaw.org/)
    is a survey of existing and proposed laws and regulations on
    cryptography.  This survey gives an overview of the current state
    of affairs, with entries per country on import/export controls,
    domestic laws, developments to restrict cryptography, and
    developments favoring crypto use. It was previously updated every
    year, but the last online edition is from February 2013.

# Forensic tools {forensic_tools}
You find some Forensic open source distributions referenced in the
section [Forensic Distributions
](/node/lightweight_distributions#forensic_distributions "internal reference")
like [Kali Linux](/node/lightweight_distributions#kali "internal reference")
and [REMnux](/node/lightweight_distributions#remnux "internal reference").

-   Wikipedia: [w:Computer forensics], [w:Digital forensic process],
    [w:List of digital forensics tools], [w:Mobile device forensics],
    [w:Network forensics]
-   [Kali list of tools
    ](http://tools.kali.org/tools-listing)
    each tool name reference a page describing it.
-   [REMnux list of tools](https://remnux.org/docs/distro/tools/)
    the use of the tool are summarized in the
    [Usage Tips for Malware Analysis on Linux
    ](https://zeltser.com/remnux-malware-analysis-tips/).
-   [Debian Administrator's Handbook: Chapter 14. Security
    ](https://debian-handbook.info/browse/stable/security.html).

-   [The Sleuth Kit](http://www.sleuthkit.org/sleuthkit/)
    (Common Public License, GPL and BM open source license)
    also known as TSK, is a collection of UNIX-based
    command line tools written in C and Perl for file and volume
    system forensic analysis.

    The Sleuth Kit supports DOS partitions, BSD partitions, Mac
    partitions, Sun slices, and GPT disks. The supported filesystems
    are NTFS, FAT, exFAT, HFS+, Ext3, Ext4, UFS and YAFFS2.
    _there is some work to implement btrfs support_.
    The Sleuth Kit is in Debian.

    -   [The Sleuth Kit Wiki](http://wiki.sleuthkit.org/)
    -   [The Sleuth Kit Wiki GitHub source repository
        ](https://github.com/sleuthkit/sleuthkit/)
-   [Autopsy](http://www.sleuthkit.org/autopsy/v2/)
    Autopsy Forensic Browser is a graphical interface to
    the command line digital forensic analysis tools in The Sleuth
    Kit. It is written in Perl. It is in Debian.
    -   Unix can run autopsy v2 but version 3 is only windows.
-   [Tiger](http://savannah.nongnu.org/projects/tiger/) (GPL)
    is a set of Bourne shell scripts, C programs and data files which
    are used to perform a security audit.  The tools rely on
    specialised external security tools such as John the Ripper,
    Chkroot and integrity check tools (like Tripwire, Integrit or
    Aide) for some of the tasks. Debian's TIGER add Debain specific
    tests: md5sums checks of installed files, location of files not
    belonging to packages, and analysis of local listening processes.
    Tiger is in Debian.

# Policy Kit

[w:PolicyKit] is a component for controlling system-wide privileges,
it replaces _sudo_.

-   [PolicyKit Home at freedesktop.org
    ](http://www.freedesktop.org/wiki/Software/PolicyKit)
-   [Polkit Documentation at freedesktop.org
    ](http://hal.freedesktop.org/docs/polkit)

# Hardened kernel and distribution.

-   [grsecurity](http://grsecurity.net/) is a security enhancement to
    the Linux kernel. It use [w:Role-based access control] (RBAC) and
    limit chroot. It can be [used in Debian
    ](https://wiki.debian.org/grsecurity) through unofficial repositories.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
