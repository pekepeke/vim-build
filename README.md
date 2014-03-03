# NAME

vim-build - vim builder

# SYNOPSIS


1. install as vimenv plugin
    $ git clone git://gihub.com/yasu-n/vim-build.git ~/.vimenv/plugins/vim-build

2. install specific version vim binary
    $ vimenv install <version>

    if you install from tarball, using -f option
    
    $ vimenv install -f vim.tar.bz2 -- <configure-options>

3. change output directory( in ~/.vimenv/versions/)
    $ vimenv install -o <output_directory>
       vim binary was output ~/.vimenv/versions/<output_directory>

4. if you want to customize configure options, please edit ~/.vimenv/share/option
     (default option is located at vim-build/share/option)

    $ mkdir ~/.vimenv/share
    $ vim ~/.vimenv/share/option

```bash
--with-features=huge
--enable-fail-if-missing
--enable-multibyte
--enable-gui=gtk2
--enable-rubyinterp
--enable-pythoninterp
--enable-python3interp
--enable-perlinterp
--enable-tclinterp
--enable-mzschemeinterp
--enable-luainterp
--with-luajit
--with-lua-prefix=/usr
--enable-gpm
--enable-xim
--enable-cscope
--enable-fontset
```

    $ vimenv install v7.4.169

5. if you want to apply patch, please edit ~/.vimenv/share/p1_patches.
     you must write the urls of patch file on p1_patches.
    $ mkdir ~/.vimenv/share
    $ vim ~/.vimenv/share/p1_patches

```bash
## commented out
# https://bitbucket.org/k_takata/vim-ktakata-mq/raw/98482edd59b30091f30371dcadad4e3ffcc132be/vim-7.4.035-breakindent.patch
https://bitbucket.org/koron/vim-kaoriya-patches/raw/6658116d59073a4471a83fea41a0791718773a96/X010-autoload_cache.diff
https://gist.github.com/Shougo/5654189/raw
```

    $ vimenv install v7.4.169

6. if you want to set variables, please edit ~/.vimenv/share/setenv
    $ mkdir ~/.vimenv/share
    $ vim ~/.vimenv/share/setenv

```bash
export vi_cv_path_perl=/usr/bin/perl
export vi_cv_path_python=/usr/bin/python
export vi_cv_path_python3=/usr/bin/python3
export vi_cv_path_ruby=/usr/bin/ruby2.0
```

    $ vimenv install v7.4.169

# DESCRIPTION

  vim-build is an [vimenv](https://github.com/raa0121/vimenv) plugin that
  provides an `vimenv install` command to compile and install latest version
  of vim on Unix-like systems.

