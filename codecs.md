<!--
.. description:
.. date: 2015-04-08
.. slug: codecs
.. tags:
.. link:
.. book: mzlinux
.. title: Media Codecs
-->

[TOC]


A [w:codec] allow to encode/decode some audio or video analog audio
signals into digital signals for transmission and storage.

# Digital Signal Processing (DSP)

-   [Comp.dsp Frequently Asked Questions
    (FAQs)](http://www.bdti.com/faq/dsp_faq.htm) _2007_
-   [Introduction to DSP](http://www.bores.com/courses/intro/)The BORES
    Signal Processing DSP course: basics, time domain processing,
    frequency analysis, filtering, IIR filters, DSP processors
-   [The Scientist and Engineer's Guide to Digital Signal Processing
    ](http://www.dspguide.com/) a free online book.
-   [Rudiments d'acoustique et de traitement du signal
    ](http://www.linuxfocus.org/Francais/March2003/article271.shtml)
-   [Brüel & Kjær's Primers](http://www.bksv.com/Library/Primers.aspx)
    provide introductions to sound and vibration measurement.

# Audio Coding and Libraries

-   [Audio File Format FAQ](http://sox.sourceforge.net/AudioFormats.html)
-   [ccrma guides](http://ccrma.stanford.edu/guides/planetccrma/)
-   [Dilettante's Dictionary](http://www.dilettantesdictionary.com/)
    an audio terminology dictionary
-   The Jason Woodard
    [Audio File Formats page of the AudioCodingWiki](http://www.audiocoding.com/modules/wiki/)
    gives a description ao each coding format.

    The
    [Speech Coding](http://www-mobile.ecs.soton.ac.uk/speech_codecs/)
    page give an idea of the principles involved in speech coding, and
    details of commonly used coders.
-   lecture notes from Dr David Marshall _2003_:
    [Multimedia Data
    ](http://www.cs.cf.ac.uk/Dave/Multimedia/node141.html),
    [Video and Audio Compression
    ](http://www.cs.cf.ac.uk/Dave/Multimedia/node200.html#SECTION04200000000000000000)
-   Wikipedia pages:
    [w:Audio file format],
    [Audio\_Codec](http://en.wikipedia.org/wiki/Audio_Codec),
    [List\_of\_odecs](http://en.wikipedia.org/wiki/List_of_codecs),
    [w:List of open-source codecs],
    [Audio\_data\_compression](http://en.wikipedia.org/wiki/Audio_data_compression),
    [x:Transcoding]
-   [ArchWiki: Codecs](https://wiki.archlinux.org/index.php/Codecs) is
    a list of codecs with links to home pages.
-   [Open Sound System (OSS)](http://www.opensound.com/oss.html)
    provides a uniform API across UNIX architectures. It is used by the
    [Open Sound System Applications](http://www.opensound.com/ossapps.html)
-   The coding use a _sample frequency_ to sample the sound, digital audio.
    The [w:Nyquist–Shannon sampling theorem|Nyquist-Shannon theorem]
    stipulates that the sampling rate must be equal to or greater than
    twice the maximum frequency contained in the signal.

    common sampling rates are:
    * 8 kHz - telephone, adequate for human speech
    * 22.050 kHz - radio
    * 32 kHz: for digital FM radio (band-limited to 15 kHz)
    * 44.100 kHz - compact disc
    * 48 kHz:  digital multitrack recording, DAT or MiniDisc  recording equipment

    [w:Sample rate conversion] _resampling_ is used to move from one rate to another one.
-   The size of a computer sound file is

         sampling rate x number of bits per sample x number of seconds x number of channels

    for a compressed lossy format it is:

         bit rate  x number of seconds x number of channels

# Lossless data compression codecs

-   Wikipedia:
    [w:List_of_codecs#Lossless_data_compression|List of codecs: Lossless data compression],
    [w:Lossless data compression]

# Lossy encoded general purpose Audio Formats (Mpeg-x)

-   Wikipedia:
    [w:List_of_codecs##Lossy_data_compression|Wikipedia List of codecs: Lossy data compression],
    [w:Lossy compression]
-   [mpeg.org](http://www.mpeg.org/) is an extensive index of MPEG
    resources with a lot of [Video](http://www.mpeg.org/MPEG/video/),
    -   [Audio](http://www.mpeg.org/MPEG/audio/)
    -   [Systems](http://www.mpeg.org/MPEG/systems/) technical resources.
-   [How audio codecs work - Psychoacoustics
    ](http://www.audiodesignline.com/showArticle.jhtml?articleID=175800470)
explaines the basics of lossy encoding.
-   [VLC: MPEG page](https://wiki.videolan.org/MPEG/)
-   [Home page of the Moving Picture Experts Group (MPEG)
    ](http://mpeg.chiariglione.org/),
    a working group of ISO/IEC with the mission to develop standards
    for coded representation of digital audio and video and related
    data.

## [w:MPEG-1]

MPEG-1 audio standardizes three different coding schemes for
digitized sound waves called Layers I, II, and III. The encoded
sound bitstream can be stored together with an encoded video
bitstream and other data streams in a so-called MPEG-1 systems
stream.

The three layers are of increasing coding/decoding complexity,
and of decreasing bit rates

Originally, the file extension ".mp3" was used for MPEG-1 Layer
III encoded sound files,and later on used also for MPEG-2 lower
sampling rate extension of Layer III.

MPEG-1 support bit rates from 32 kbit/s to 320 kbit/s.

Variable bitrate is part of the standards of layer-III and also
supported by most of the encoders/decoders of layers I and II

Refs:
-   [Wikipedia: MPEG-1](http://en.wikipedia.org/wiki/MPEG-1)
-   Mpeg-1 is decribed in
    [MPEG Audio FAQ](http://www.tnt.uni-hannover.de/project/mpeg/audio/faq/mpeg1.html)

## [w:MPEG-2]

The first phase, MPEG-1, was dealing with mono and two-channel
stereo sound coding, at sampling frequencies commonly used for high
quality audio (48, 44.1 and 32 kHz). The second phase, MPEG-2
supports three extensions:

-   extension to lower sampling frequencies (16 kHz, 22.05 kHz
    and 24 kHz), providing better sound quality at very low bit rates
    (below 64 kbit/s for a mono channel),
-   extension of MPEG-1 to multichannel sound. MPEG-2 BC supports
    up to 5 full bandwidth channels plus one low frequency enhancement
    channel (referred to as '5.1'). This multichannel extension is both
    forward and backward compatible with MPEG-1, an MPEG-2 BC stream
    can be read and interpreted by an MPEG-1 audio decoder. Like MPEG-1
    the first two workitems of MPEG-2 have the three layer structure,
    the original MPEG-2 audio standard contained only the first
    workitems was finalized in 1994.
-   A new coding scheme called "Advanced Audio Coding" (AAC) not
    backward compatible with MPEG-1.It improve coding efficiency for
    the 5-channel case and was finalized in 1997. It provides very high
    audio quality at a rate of 64 kb/s/channel for multichannel
    operation. It provides a capability of up to 48 main audio
    channels, 16 low frequency effects channels, 16
    overdub/multilingual channels, and 16 data streams.AAC adheres to
    the same basic coding paradigm as MPEG-1/2 Layer-3, but adds new
    coding tools and improves on details. As a result, AAC is
    approximately 30% more bit rate efficient than MPEG-1 Layer 3.

    The [w:High Efficiency Advanced Audio Coding] part of AAC is
    included in [w:MPEG-4 Part 3].

Refs:

-   Wikipedia: [w:MPEG-2], [w:Advanced Audio Coding] (AAC)
-   A full description of MPEG-2 and AAC is in the
    [MPEG Audio FAQ
    ](http://www.tnt.uni-hannover.de/project/mpeg/audio/faq/mpeg2.html)

## [w:MPEG-4]

[w:MPEG-4 Audio] or _MPEG-4 Part 3_ provides tools for coding of both natural and
synthetic audio objects. The representations provide compression
and other functionalities, such as scalability or play-back at
different speeds.

MPEG-4 is used for playing multiple audio objects like the
instruments of an orchestra, the multilingual language streams,or
movie applications.( there is also a multilingual/ multiprogramme
capability in MPEG-2 AAC, and a multilingual capability in the
MPEG-2 BC audio coding standard.)


[w::MPEG-4 Part 14] or MP4 is a container format most commonly
used to store video and audio, but can also be used to store other
data such as subtitles and still images.

Refs: [Wikipedia: MPEG-4](http://en.wikipedia.org/wiki/MPEG-4).

### [w:H.264 or MPEG-4 Part 10] {#H264}
[w:H.264 or MPEG-4 Part 10], Advanced Video Coding (MPEG-4 AVC) is a block-oriented
motion-compensation-based video compression standard. As of 2014, it is one of the most
commonly used formats for the recording, compression, and distribution of video
content.[1] It supports resolutions up to 8192×4320

-   [w:List of video services using H.264/MPEG-4 AVC]

## MPEG-7

Where MPEG-1 and -2 concentrated almost entirely on
compression, MPEG-4 moved to a higher level of abstraction in
coding objects, MPEG-7 moves to description of meta-information on
sound. example application areas of MPEG-7 audio are: setting-up
audio archives (radio, movies, tv), retrieving audio files from the
Internet/from an archive, filtering audio broadcasts, music
education, surveillance.

-   [MPEG-7](http://www.tnt.uni-hannover.de/project/mpeg/audio/faq/mpeg7.html)


## MP3

MPEG-1/2 Layer III, became the de-facto standard for lossy
audio encoding, due to the high compression rates (1/12 of the
original size, still retaining considerable quality), the high
availability of decoders and the low CPU requirements for playback
(a 486 DX2-66 is enough for real-time decoding). It supports
multichannel files with the MPEG-2 "BC" standard (although there's
no publicly available implementation of this backward-compatible
version), sampling rates from 16kHz? to 24kHz? (MPEG-2 Layer III)
and 32kHz? to 48kHz? (MPEG-1 Layer III).

MP3 has been enhanced by
[w:MP3Pro]
i.e. MPEG-1 Layer III combined with SBR

Refs:

-   [Wikipedia: MP3](http://en.wikipedia.org/wiki/MP3).
-   [MP3 Tech](http://www.mp3-tech.org/)
-   BBC [Guide to the MP3 File Conversion Process](http://www.bbc.co.uk/dna/h2g2/A14171988)
-   Technical info at
    [digital-audio.com](http://www.digital-audio.net/technical.shtml)
-   [Lame Documentation](http://lame.sourceforge.net/)
-   [HydrogenAudio Lame recommended settings
    ](http://wiki.hydrogenaud.io/index.php?title=Recommended_LAME)
-   [Audacity Wiki: MP3](http://wiki.audacityteam.org/wiki/MP3)
-   Two old _2001_ how-tos:
    [MP3 HOW-TO](http://www.tldp.org/HOWTO/MP3-HOWTO.html),
    [MP3 CD Burning mini-HOWTO](http://www.tldp.org/HOWTO/MP3-CD-Burning/).


### mp3 quality versus bitrate

From [MP3 Tech](http://www.mp3-tech.org/) listening tests for music
96kb/s quality clearly differ from original and even 128kb/s has some
difference 256kb/s is identical.

The conlusion is: For a computer use, the 128kbs rate produces a
quality equal to an audio CD. But in the case of an MP3 use in
advanced Hi-Fi, it is necessary to use a 256kbs bitrate to reach an
identical result to the CD sound.

In HydogenAudio recommendation we find:

For very high quality: HiFi, home, or quiet listening, with best file size
:   -V0 (~245 kbps), -V1 (~225 kbps), -V2 (~190 kbps) or -V3 (~175
    -kbps) are recommended.
Listening in noisy conditions, lower bitrate, smaller file size:
:   V4 -(~165 kbps), -V5 (~130 kbps) or -V6 (~115 kbps) are recommended.
    -V6 produces an "acceptable" quality,
    while -V4 should be close to perceptual transparency.
Very low bitrate, small sizes: eg. for voice, radio, mono encoding etc.
:   For very low bitrates, up to 100kbps, ABR is most often the best
    solution. Use --abr <bitrate> (e.g. --abr 80).


For sample rates choice we find in
[audacity Wiki: sample rates](http://wiki.audacityteam.org/wiki/Sample_Rates)

-   44.1 kHz (44100 Hz) audio CDs giving a 20 kHz maximum frequency.
    choice for high quality tape decks, and medium quality LP
    equipment which can reproduce 20 kHz. Note that many older
    people cannot hear above 14.5kHz.
-   48 kHz (48000 Hz) is the sample rate used for DVDs.
-   32 kHz / 14.5 kHz limit of ferric cassette tape, little below FM
    radio bandwidth, so FM radio can be recorded with only a little
    quality loss.
-   22.05 kHz, 10 kHz: For speech recording where perceived quality
    is unimportant, but clarity must be maintained and  AM radio.
-   8 kHz / 3.6 kHz: 3.6 kHz matches the bandwidth of telephone
    sytems. Used for telephone speech,  microcassette recording.

    Sound quality is terrible, with speech as clear as a mud bath. Any
    further drop in sample rate makes intelligibility a challenge.

## Philips voice tracer predefined settings.
My Philips voice tracer encodes at 32000 Hz 96 kb/s, or 22050 Hz 64
kb/s.



## Table of bitrates

           |--------------+-------------+-------------------------+
           |      Bitrate |   Bandwidth | Quality comparable to   |
           |--------------+-------------+-------------------------|
           |      16 kbps |     4.5 kHz | shortwave radio         |
           |--------------+-------------+-------------------------|
           |      32 kbps |     7.5 kHz | AM radio                |
           |--------------+-------------+-------------------------|
           |      96 kbps |      11 kHz | FM radio                |
           |--------------+-------------+-------------------------|
           |     128 kbps |      16 kHz | near CD                 |
           |--------------+-------------+-------------------------|
           | 160-180 kbps |      20 kHz | perceptual transparency |
           | (variable  ) |             |                         |
           |--------------+-------------+-------------------------|
           |     256 kbps |      22 kHz | studio                  |
           |--------------+-------------+-------------------------+

    sample 5mn 48000hz stereo 57.60M
    flac 24.36M
    ogg quality
    -q1   2.64M
    default -q 3 3.34M
    -q7   5.66M
    -q9   8.88
    -q10 12.05M
    mono quality  default (-q3) 2.48M
    16Khz  quality  (-q5) 2.00M
    16Khz  quality default (-q3) 1.61M
    16Khz  quality  (-q0) 1.21M
    16Khz mono quality default (-q3) 1.22M

    speex  default quality (--quality 8) 48000hz 2.12M
    32000hz (-u) 1.42M
    16000hz (-w) 1.10M
    16000hz (-w) --vbr (default is constant bit rate) 0.97M
    16000hz (-w) --quality 5 0.69M
    16000hz (-w) --quality 3  0.42M
    8000hz (-n)  0.61M
    8000hz mono 0.58M

    mp3 constant bit rate 128kHz 4.8M
    vbr -q 4 3.7M

    Example 97mn42 16000Hz mono (tape)
    raw 187.6 M
    ogg q3 23.6M (32kbps)
    ogg q1 18.9M (26kbps)
    speex q5 vbr 11.5M
    speex q5 fbr 13M
    speex q8 (default) vbr  15.4M
    speex q8 (default fbr)  20.9M (encoding 20mn cpu!)
    the quality for vbr is awfull (q8 as q5)

"WAVE audio, IMA ADPCM, mono 8000 Hz" is 1/4 of "WAVE audio,
Microsoft PCM, 16 bit, mono 8000 Hz"
PCM 16 bits 8000 Hz is encoded at 1/40 in mp3 128 b/s

## [w:Advanced Audio Coding] (AAC)

Advanced Audio Coding, the format for general audio coding in
both MPEG-2 and MPEG-4 standards is an advanced audio coding
devived from ISO/MPEG Audio Layer-3 (
[Fraunhofer's AAC info page](http://www.iis.fraunhofer.de/amm/techinf/aac/index.html))

[AudioCoding.com](http://www.audiocoding.com/)
provide free MPEG-4 audio codecs. Currently implemented are MPEG-2
and MPEG-4 AAC. The supported AAC profiles are HE, Main, LC, LTP
and LD.

AAC can be encoded whith [FAAC](#item_faac) and decoded by
[FAAD2](#item_faad2)

MPEG-4 AAC combined with Spectral Band Replication / SBR is
refereed by AAC+.

Refs:

-   [Wikipedia: Advanced Audio Coding (AAC)
    ](http://en.wikipedia.org/wiki/Advanced_Audio_Coding).

## [w:ATRAC]

Adaptive Transform Acoustic Coding, used in Sony's MiniDisc
(MD) recorders, an RealAudio 8 compression format. They encode
from ATRAC1 Stereo 292 kbps to ATRAC3 Stereo Longplay 4x (LP4) 66
kbps

## [Ogg Vorbis](http://en.wikipedia.org/wiki/Ogg_vorbis) {#ogg_vorbis}

Vorbis is a general purpose perceptual audio unpatented CODEC.
At the high quality/ bitrate end of the scale (CD or DAT rate
stereo), it is in the same league as MPEG-4 (AAC), and similar to,
but higher performance than MPEG-1/2 audio layer 3, MPEG-4 audio
(TwinVQ), WMA and PAC. Similarly, the 1.0 encoder can encode
high-quality CD and DAT rate stereo at below 48 kbps without
resampling to a lower rate. Vorbis is also intended for lower and
higher sample rates (from 8 kHz telephony to 192 kHz digital
masters) and a range of channel representations (monaural,
polyphonic, stereo, quadraphonic, 5.1, ambisonic, or up to 255
discrete channels).

Ogg vorbis use a *quality* factor instead of average bit rate.  This
quality is explained in the
[Ogg Vorbis FAQ](http://vorbis.com/faq/#quality):

*quality 0 is roughly equivalent to 64kbps average, 5 is roughly
160kbps, and 10 gives about 400kbps. Most people seeking
very-near-CD-quality audio encode at a quality of 5 or, for lossless
stereo coupling, 6. The default setting is quality 3, which at
approximately 110kbps gives a smaller filesize and significantly
better fidelity than .mp3 compression at 128kbps.*.

Some comparison is also given in
[Wikipedia Ogg Vorbis page](http://en.wikipedia.org/wiki/Ogg_vorbis).

Refs:

-   [xiph.org: Ogg Vorbis](http://www.xiph.org/vorbis/)
-   [vorbis.com](http://www.vorbis.com/)

## [w:Opus_(audio_format)|Opus] {#opus_codec}
Opus is a lossy audio coding format developed by the Internet
Engineering Task Force (IETF).

Opus has a very low algorithmic delay or latency, 26.5 ms by default,
and even by trading-off quality or bitrate it achieves very low delay,
down to 5 ms.  It is better than the 30ms of Speex, and MP3, Ogg
Vorbis and HE-AAC use a delay well over 100 ms.  The inherently low
delay in Opus makes it possible to be used in the same real-time
applications required by telephony, Voice over IP and
videoconferencing.

Opus codec support is implemented in the reference implementation
_opus-tools_ and in GStreamer, FFmpeg and Libav libraries.

Through these libraries many players support opus:
Amarok, clementine, exaile, cmus, moc, mpd, SMplayer, VLC media player...

Opus is supported in HTML5 browsers like Mozilla Firefox, Chromium and
Google Chrome, Blink-based Opera.

Devices based on Google's Android platform, as of version 5.0
"Lollipop", support the Opus codecs. Chromecast supports Opus
decoding.

Opus data can be encapsulated in Ogg, Matroska, WebM
(which is a subset of Matroska), and MP4 containers.
The content of an Ogg Opus streams should be specified as
`audio/ogg; codecs=opus` and use `.opus` as filename extension.

[ietf draft: Ogg Encapsulation for the Opus Audio Codec
](https://tools.ietf.org/id/draft-ietf-codec-oggopus-08.html)
gives the [comment header packet
](https://tools.ietf.org/id/draft-ietf-codec-oggopus-08.html#rfc.section.5.2)
it is the same as Ogg/Vorbis.

The [ Opus Codec - Comparison
](https://opus-codec.org/comparison/) page give a comparison
of codecs.

Opus at 16Kb/s is equivalent to speex at 32kb/s.  Opus at
32kb/s is equivalent to vorbis 48kb/s or mp3 64kb/s, the only other
quality encoding is the proprietary [w:AMR-WB] used by QuickTime,
RealPlayer.

Opus at 64kb/s is equivalent to vorbis 96 kb/s or mp3 128
kb/s.  There is no much difference between opus, aac, and vorbis at
128kb/s and they are only slightly better than mp3 128 kb/s.

At all frequencies above 32kb/s the proprietary AAC and opus are very
close.

The [Opus page of Hydrogenaudio
](http://wiki.hydrogenaud.io/index.php?title=Opus) and
the [Opus Recommended Settings from Xiph.org
](https://wiki.xiph.org/Opus_Recommended_Settings)
recommend for VoIP 10 to 24 kbs with a bandwidth of 6kHz to 8 kHz, for
podcasts or audiobooks 32kps mono or 36kbs to 40 kbs
stereo achieving a bandwidth of 12 kHz;
64kbs for stereo music storage & streaming with 20 kHz bandwidth,
and 96kbs to approach transparency, comming very close at 128kbps.

Refs:
-   [w:Opus_(audio_format)|Wikipedia: Opus]
-   [Opus Home](https://opus-codec.org/)
-   [Opus FAQ](https://wiki.xiph.org/OpusFAQ)

## [w:Musepack] or MPC
MPC or Musepack, formerly known as MP+ or MPEGplus, is based on
the MPEG-1 Layer-2 / MP2 algorithms. It contains heavily optimized
and patentless code. MPC is an open encoder/decoder with very fast
encoding/decoding wich rank between Ogg (1rst) and MP3 for
transparency. MPC is single channel and not streamable.
Refs:
[Wikipedia Musepack](http://en.wikipedia.org/wiki/Musepack)

## [w:Windows Media Audio] (WMA)
proprietary audio data compression technology developed by Microsoft.

## Other lossy format

From [w:Dolby] we have__AC-2__
Audio Coding Version 2 from Dolby, [w:Dolby Digital] (AC-3 or AC3)
Audio Coding Version 3 from Dolby, RA: RealAudio
proprietary streamable multimedia format from RealNetworks, AMB
Ambisonics, DTS: Digital Theatre System, ECM ECAM audio
compression, SDDS Sony Dynamic Digital Sound, VQF also known as
TwinVQ

# Lossy encoded voice Audio Formats - Vocodecs

Narrowband speech codecs are used to give an efficient digital
representation of telephone bandwidth speech. Often the speech is
bandlimited to between 200 and 3400 Hz, and is sampled at 8 kHz. An
ideal speech codec will represent this speech with as few bits as
possible, while producing reconstructed speech which sounds identical,
or almost identical, to the uncoded speech.


Speech codecs are described in
[Speech Coding](http://www-mobile.ecs.soton.ac.uk/speech_codecs/index.html) page
of the University of Southampton

Wikipedia has a [w:List_of_codecs#Voice|list of voice codecs] and a
page on [w:Speech coding].


mu-law and a-law [PCM](http://www-mobile.ecs.soton.ac.uk/speech_codecs/standards/pcm.html)
:   PCM can have their bit rates reduced by using non-uniform
    quantization of the samples. In speech coding an approximation to a
    logarithmic quantizer is often used. Such quantizers give a signal
    to noise ratio which is almost constant over a wide range of input
    levels, and at a rate of eight bits/sample (or 64 kbits/s) give a
    reconstructed signal which is almost indistinguishable from the
    original. In America u-law companding is the standard, while in
    Europe the slightly different A-law compression is used.

[ADPCM](http://www-mobile.ecs.soton.ac.uk/speech_codecs/standards/adpcm.html)
:   If we attempt to predict the value of the next sample from the
    previous samples then the error signal between the predicted samples
    and the actual speech samples will have a lower variance than the
    original speech samples. Therefore we should be able to quantize
    this error signal with fewer bits than the original speech signal.
    This is the basis of Differential Pulse Code Modulation (DPCM)
    schemes. They are mproved if the predictor and quantizer are made
    adaptive. This leads to Adaptive Differential PCM (ADPCM) codecs.
    ADPCM codec operating at 32 kbits/s,gave speech quality that was
    very similar to the 64 kbits/s PCM codecs.Codecs operating at 16,24
    and 40 kbits/s are also standardised.

[GSM](http://www-mobile.ecs.soton.ac.uk/speech_codecs/standards/gsm.html)
:   The "Global System for Mobile communications" (GSM) operates at 13
    kbits/s. Its main advantage over other low rate codecs is its
    relative simplicity.

[Speex](http://www.speex.org/)
:   Speex is a codec designed for compressing voice at low bitrates. It
    is not suitable for music-content. Speex uses Ogg as
    transport-layer, just like Ogg Vorbis.

# Uncompressed Sound formats

The formats are:

[w:Resource Interchange File Format] RIFF
:   better known as Microsoft WAVE file format. Actually it is a
    container format which can contain uncompressed linear PCM audio.
:   refs: [WAVE PCM soundfile format
    ](http://ccrma.stanford.edu/courses/422/projects/WaveFormat/)
    course at ccrma

[w:Audio Interchange File Format] (AIFF)
:   Audio format introduced by Apple and Sun.

[w:Pulse-code modulation] PCM

:   (linear) PCM or Pulse-Code Modulation: Modulation in which a signal is
    sampled, and the magnitude (with respect to a fixed reference) of
    each sample is quantized and digitized. Narrow-band speech is
    typically band-limited to 4 kHz and sampled at 8 kHz. If linear
    quantization is used then to give good quality speech around twelve
    bits per sample are needed, giving a bit rate of 96 kbits/s.

The format of words under x86 is low endian (cf endian.h), so the wave
and raw files will be stored as low endian, nevetherless Sun/NeXT audio
data are always big endian, oggenc has a default of lowendian that can
be changed by `--raw-endianness` (big endian (1) or little endian (0)),
and lame default to native endianness, (little endian here) and use -x
to swap bytes.

The sound is set in mono/stereo by using `-c n` in sox and
aplay/arecord, `-C n` in oggenc, `-m m` for mono in lame and `-m s/j/f`
or even `-m s -a` for stereo input, where the different options give the
output encoding of stereo, joint stereo, forced joint stereo, dual
channels and mono (ref: [lame(1)
](http://manpages.debian.org/cgi-bin/man.cgi?query=lame(1)))


The frequency is given by `-r hertz` in sox and aplay/arecord,
`-R hertz` in oggenc and `-s KHertz` in lame

The sound can be stored as signed or unsigned linear (-s/-u for sox) and
in bytes words or long words ( -b/-w/-l for sox) this can also be
specified by a bit number( --bitwidth for lame, --raw-bits for oggenc)
the combined sign+length+endianess gives for arecord/aplay
`S8 U8 S16_LE S16_BE U16_LE U16_BE S24_LE S24_BE U24_LE U24_BE S32_LE S32_BE U32_LE U32_BE`

Refs:

-   [PCM
    ](http://www-mobile.ecs.soton.ac.uk/speech_codecs/standards/pcm.html)

# Sound info
 <a name="ffprobe"></a>[ffprope](/node/ffmpeg "internal reference")
:   _ffprobe_ is part of [ffmpeg](/node/ffmpeg "internal reference")

       ffprobe -hide_banner "/path/to/input"

    If your distibution rather provide
    [libav](/node/ffmpeg#libav "internal reference") use:

        avprobe /path/to/input

id3info
:   [id3info(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=id3info(1))
    from the
    [id3lib](/node/tag_management) library displays
    both the id3v1 and id3v2 tag information for a file, along with the
    sample rate, and bitrate. *id3info* is packaged in Debian/Ubuntu in
    the *libid3-x-dev* package.

midentify
:   To get info about a sound or video file using
    [mplayer](/node/media_players#mplayer "internal reference") :

        mplayer -vo null -ao null -frames 0 -identify <file> 2>/dev/null

    If you need a cleaner output for use in script, you can use a simple
    sed filter.

        sed -ne '/^ID_/ { s/[]()|&;<>`'"'"'\\!$" []/\\&/g;p }'

    And it constitutes the *midentify.sh* that lies in the
    [Tools directory of mplayer svn repository
    ](http://svn.mplayerhq.hu/mplayer/trunk/TOOLS/README?view=co)
    , but is not incorporated in a lot of mplayer packages.

    _Now you can replace it with
    [ffmpeg/libav](#avprobe "internal reference")_

mp3info
:   mp3info can display ID3 1.x tag information as well as various
    technical aspects of an MP3 file including playing time, bit-rate,
    sampling frequency
ogginfo
:   Ogginfo from the [VorbisTools](/node/sound_edit#vorbistools) package
    gives info from vorbis streams, including the sample rate and number
    of channels, the bitrate and playback length, and the contents of
    the comment header.

sfinfo
:   `sfinfo`  from [audiofile library
    ](/node/sound_libs#audiofile "internal reference")
    gives informations on a supported sound file (format, rate,
    size, duration).

sndfile-info
:   The command [sndfile-info
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=sndfile-info(1))
    from [libsndfile](/node/sound_libs#libsndfile "internal reference")
    display basic information about a sound file such as its format,
    its sample rate, and the number of channels.
    This information is obtained using
    [libsndfile](/node/sound_libs#libsndfile "internal reference")
    for the supported formats
    *(mainly lossless encoding formats)*

soxi
:   is part of [sox](/node/sound_edit#sox "internal reference")
    [soxi(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=soxi)

sndinfo
:   `sndinfo` wich comes with the [Snd](/node/sound_edit#snd) editor gives
    informations on a sound file (format, rate, size, duration).


# Codecs support in multmedia libraries

Seee also [FFmpeg & Libav section](/node/ffmpeg "internal reference").

-   [ArchLinux Codecs](https://wiki.archlinux.org/index.php/Codecs)
    list codecs and application backends;
-   [Debian Wiki: MultimediaCodecs
    ](https://wiki.debian.org/MultimediaCodecs).


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
