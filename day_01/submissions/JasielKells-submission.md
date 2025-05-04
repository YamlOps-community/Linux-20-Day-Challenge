Linux Day_01 Activity

# pwd
kells@kells-HP-EliteBook-Folio-1040-G1:~/Documents/Linux-20-Day-Challenge/day_01/submissions$ pwd
/home/kells/Documents/Linux-20-Day-Challenge/day_01/submissions

# cd
kells@kells-HP-EliteBook-Folio-1040-G1:~/Documents/Linux-20-Day-Challenge/day_01/submissions$ cd ..
kells@kells-HP-EliteBook-Folio-1040-G1:~/Documents/Linux-20-Day-Challenge/day_01$

# ls
kells@kells-HP-EliteBook-Folio-1040-G1:~/Documents/Linux-20-Day-Challenge/day_01/submissions$ ls
AdetokunAdenike.md                ChinonsoNwakudu-submission.md  tobilol-submission
aminatanimashaun31-submission.md  davidoyewole.md                utibe-submission
cf-cloud89-submission.md          JasielKells-submission.md      williethedeveloper-submission.md
chemben17-submission.md           obasoro-submission
chinaecheremMba-submission.md     Okumraymond-submission.md

# whoami
kells@kells-HP-EliteBook-Folio-1040-G1:~/Documents/Linux-20-Day-Challenge/day_01/submissions$ whoami
kells

# man
kells@kells-HP-EliteBook-Folio-1040-G1:~/Documents/Linux-20-Day-Challenge/day_01/submissions$ man git

GIT(1)                                              Git Manual                                             GIT(1)

NAME
       git - the stupid content tracker

SYNOPSIS
       git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p|--paginate|-P|--no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--config-env=<name>=<envvar>] <command> [<args>]

DESCRIPTION
       Git is a fast, scalable, distributed revision control system with an unusually rich command set that
       provides both high-level operations and full access to internals.

       See gittutorial(7) to get started, then see giteveryday(7) for a useful minimum set of commands. The Git
       User’s Manual[1] has a more in-depth introduction.

       After you mastered the basic concepts, you can come back to this page to learn what commands Git offers.
       You can learn more about individual Git commands with "git help command". gitcli(7) manual page gives you
       an overview of the command-line command syntax.

       A formatted and hyperlinked copy of the latest Git documentation can be viewed at
  
GIT(1)                                              Git Manual                                             GIT(1)

NAME
       git - the stupid content tracker

SYNOPSIS
       git [-v | --version] [-h | --help] [-C <path>] [-c <name>=<value>]
           [--exec-path[=<path>]] [--html-path] [--man-path] [--info-path]
           [-p|--paginate|-P|--no-pager] [--no-replace-objects] [--bare]
           [--git-dir=<path>] [--work-tree=<path>] [--namespace=<name>]
           [--config-env=<name>=<envvar>] <command> [<args>]

DESCRIPTION
       Git is a fast, scalable, distributed revision control system with an unusually rich command set that
       provides both high-level operations and full access to internals.

       See gittutorial(7) to get started, then see giteveryday(7) for a useful minimum set of commands. The Git
       User’s Manual[1] has a more in-depth introduction.

       After you mastered the basic concepts, you can come back to this page to learn what commands Git offers.
       You can learn more about individual Git commands with "git help command". gitcli(7) manual page gives you
       an overview of the command-line command syntax.

       A formatted and hyperlinked copy of the latest Git documentation can be viewed at
       https://git.github.io/htmldocs/git.html or https://git-scm.com/docs.

# whereis
kells@kells-HP-EliteBook-Folio-1040-G1:~/Documents/Linux-20-Day-Challenge/day_01/submissions$ whereis ls
ls: /usr/bin/ls /usr/share/man/man1/ls.1.gz

# which
kells@kells-HP-EliteBook-Folio-1040-G1:~/Documents/Linux-20-Day-Challenge/day_01/submissions$ which man
/usr/bin/man

# ls -la
kells@kells-HP-EliteBook-Folio-1040-G1:~/Documents/Linux-20-Day-Challenge/day_01/submissions$ ls -la
total 72
drwxrwxr-x 2 kells kells  4096 May  4 11:07 .
drwxrwxr-x 3 kells kells  4096 May  4 09:58 ..
-rw-rw-r-- 1 kells kells   306 May  4 09:58 AdetokunAdenike.md
-rw-rw-r-- 1 kells kells   757 May  4 09:58 aminatanimashaun31-submission.md
-rw-rw-r-- 1 kells kells   749 May  4 09:58 cf-cloud89-submission.md
-rw-rw-r-- 1 kells kells   407 May  4 09:58 chemben17-submission.md
-rw-rw-r-- 1 kells kells   366 May  4 09:58 chinaecheremMba-submission.md
-rw-rw-r-- 1 kells kells   555 May  4 09:58 ChinonsoNwakudu-submission.md
-rw-rw-r-- 1 kells kells   646 May  4 09:58 davidoyewole.md
-rw-rw-r-- 1 kells kells  2467 May  4 11:07 JasielKells-submission.md
-rw-r--r-- 1 kells kells 12288 May  4 11:06 .JasielKells-submission.md.swp
-rw-rw-r-- 1 kells kells   669 May  4 09:58 obasoro-submission
-rw-rw-r-- 1 kells kells   405 May  4 09:58 Okumraymond-submission.md
-rw-rw-r-- 1 kells kells   504 May  4 09:58 tobilol-submission
-rw-rw-r-- 1 kells kells   349 May  4 09:58 utibe-submission
-rw-rw-r-- 1 kells kells   372 May  4 09:58 williethedeveloper-submission.md

