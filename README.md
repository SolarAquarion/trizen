trizen
======

trizen is a lightweight wrapper for AUR, written in Perl.

Main features include:
* Installation of packages from AUR
* Search support for AUR packages
* Reading AUR comments for packages
* Updating the installed AUR packages
* Recursive AUR dependencies support
* Built-in interaction with 'pacman'
* Edit support for text files
* Input/output UTF-8 support

```
usage: trizen [option] [pkgname] [pkgname] [...]

Main options:
    -S              : installs package
    -Ss             : searches for package
    -Si             : outputs info for package
    -Sm             : outputs the packages maintained by [...]
    -Sp             : outputs PKGBUILD only
    -Sl             : builds and installs package from `pwd`
    -Su             : upgrades installed packages
    -Sc             : clears the cache directory
    -C              : shows AUR comments for package
    -G              : clones a package in the current directory
    -Gd             : clones a package with all needed AUR dependencies
    -R              : removes packages (see pacman -Rh)
    -Q              : for installed packages (see pacman -Qh)
    -U              : installs local packages from `--clone-dir` or `pwd`

Other options:
    --quiet         : be quiet
    --really-quiet  : be really quiet
    --nocolors      : no text colors
    --aur           : only AUR packages (with -S, -Si, -Su, -Ss)
    --asdep         : installs package as dependency
    --movepkg       : move the built package to the pacman cache directory
    --needed        : do not reinstall up-to-date packages
    --noedit        : do not prompt to edit files
    --nopull        : do not `git pull` new changes
    --nobuild       : do not build packages (implies --noedit)
    --noinstall     : do not install package after building
    --noinfo        : do not display package info after cloning
    --devel         : update devel packages during -Su
    --show-ood      : show out-of-date flagged packages during -Su
    --noconfirm     : do not ask for any confirmation
    --force         : pass the --force option to pacman
    --skipinteg     : pass the --skipinteg option to makepkg
    --stats         : show some info about the installed packages
    --update-config : update configuration file before exit
    --clone-dir=s   : directory where to clone and build packages
    --movepkg-dir=s : move built packages in this directory (with --movepkg)

Meta options:
    --debug         : activate verbose mode
    --help          : print this message and exit
    --version       : print version and exit

** Each config-key is a valid argument when preceded by '--'

```

A configuration file is automatically generated at: `~/.config/trizen/trizen.conf`
