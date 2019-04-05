---
title: System Schedulers
---

{{% toc /%}}

# References

-   Wikipedia {{< wp "cron" >}}, {{< wp "anacron" >}}, {{< wp "inotify" >}}
-   Markus Gattol [overview of cron, anacron, ntp, chrony
    ](http://www.markus-gattol.name/ws/time.html)
    with many examples.

# cron

-   Wikipedia {{< wp "cron" >}}
-   [Gentoo: cron](https://wiki.gentoo.org/wiki/Cron)
-   [ArchWiki: cron](https://wiki.archlinux.org/index.php/Cron)
-   [Chronic](http://habilis.net/cronic/)
    shell script for wrapping cron jobs so that cron only sends email
    when an error has occurred. Cronic defines an error as any
    non-trace error output or a non-zero result code.shell script for
    wrapping cron jobs so that cron only sends email when an error has
    occurred. Cronic defines an error as any non-trace error output or
    a non-zero result code.


# Inotify {#inotify}

[inotify home page
](http://inotify.aiken.cz/?section=common&page=home&lang=en) (GPL)
Inotify is an inode-base file system notification mechanism
implementated in the linux kernel.

-   Wikipedia {{< wp "inotify" >}}
-   Michael Kerrisk in [lwn.net](https://lwn.net) has written an
    introduction to inotify structure:
    [Filesystem notification, part 1: An overview of dnotify and
    inotify][https://lwn.net/Articles/604686/),
    [part 2: A deeper investigation of inotify
    ](https://lwn.net/Articles/605128/).
-   [inotify(7) man page
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=inotify)
-   [inotify tools
    ](https://github.com/rvoicilas/inotify-tools/wiki#info)
    are tools to allow inotify's features to be used
    from within shell scripts. _inotyfy-tools is a debian package_.

    -   {{< man "inotifywatch(1)" >}} listens for filesystem events using
        Linux's {{< man "inotify(7)" >}} interface, then outputs a summary
        count of the events received on each file or directory.
    -   {{< man "inotifywait(1)" >}} waits for changes to files using
        {{< man "inotify(7)" >}} interface. It is suitable for waiting for
        changes to files from shell scripts. It can either exit once
        an event occurs, or continually execute and output events as
        they occur.

    For these two tools there are examples in the
    [inotify tools home page
    ](https://github.com/rvoicilas/inotify-tools/wiki#info)

-   [incron documentation
    ](http://inotify.aiken.cz/?section=incron&page=doc)
    incron is an "inotify cron" system.
    It consists of a daemon and a table manipulator.
    Inotify cron handles filesystem events rather than time
    periods.
-   [fsniper](https://github.com/l3ib/fsniper) (GPL)
    by Dave Foster
    is a utility that waits for a file to be changed or created,
    and then executes a command on that file.
-   [Doit](http://pydoit.org/)
    is a python build tool that integrates
    inotify
-   [Pyinotify](https://github.com/seb-m/pyinotify)
    is a Python package used for monitoring filesystems events
    with [inotify](http://inotify.aiken.cz/).
    The [pynotify documentation](https://github.com/seb-m/pyinotify/wiki)
    includes a tutorial and some examples.
    - Pynotify is used in
      [pirsyncd - Python Inotify Rsync Daemon
      ](http://ebalaskas.gr./blog/?page=pirsyncd)
      see the [pirsyncd repository](https://bitbucket.org/ebal/pirsyncd)
    - [spotter](https://github.com/borntyping/spotter) is a
      command line tool for watching files and running shell
      commands when they change. It uses pynotify.
-   [watchdog](https://pypi.python.org/pypi/watchdog)
    is a python API and shell utilities to monitor file system events.sudo
-   `tail --follow` uses inotify if available

## Knowing who consume instances

You have a list of processes and used instances with:

    find /proc/*/fd/* -type l -lname 'anon_inode:inotify' -print| sort -t/ -k3 -n

## Controlling the number of watches

You can find maximum number of inotify instances in
`/proc/sys/fs/inotify/max_user_instances` and the
maximum number of files watched in
`/proc/sys/fs/inotify/max_user_watches`

The default maximum number of inotify watches is 8192

Use `tail -f` to verify if you exceed the inotify maximum watch limit.
as it uses inotify and If you've run out of your inotify watches,
you'll get this error:

    tail: inotify cannot be used, reverting to polling: Too many open files

### Knowing the current number of watches

To  know the current number of watches added by a process
-   Enable add_watches tracing with:

        echo 1 >|\
        /sys/kernel/debug/tracing/events/syscalls/sys_exit_inotify_add_watch/enable

-   Stop the process
-   Register watches

        cat /sys/kernel/debug/tracing/trace_pipe \
            |grep '1234*inotify_add_watch' >/tmp/inotify_watches

-   Restart the process, and wait a while it setup its watches.
-   Count watches.

        wc -l /tmp/inotify_watches

-   Disable add_watches tracing with:

        echo 0 >|\
        /sys/kernel/debug/tracing/events/syscalls/sys_exit_inotify_add_watch/enable

The format is given in the file `/sys/kernel/debug/tracing/README`

You can have a list of the pids that have a inotify fd registered by

    sudo ls -l /proc/*/fd/* | grep notify

For more information on tracing look at
[kernel documentation: ftrace.txt
](https://www.kernel.org/doc/Documentation/trace/ftrace.txt).
and
[yocto project: tracing and profiling - ftrace
](https://wiki.yoctoproject.org/wiki/Tracing_and_Profiling#ftrace).

## modifying the settings

Each watch has a cost following
[this post answer](http://askubuntu.com/a/155426) and the referred
link on a 64b system it uses 1kb/watch in the unswapable kernel memory
_(half on a 32b system)_, so the standard limit of 8192 watches is
consuming 8M.

To increase the Inotify watchers limit:

-   for a temporary change:

        echo 100000 > /proc/sys/fs/inotify/max_user_watches

    or

        sysctl -w fs.inotify.max_user_watches=100000

-  for a permanent one write in `/etc/sysctl.conf`

        fs.inotify.max_user_watches=100000



<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
