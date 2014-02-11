# NAME

vim-build - vim builder

# SYNOPSIS

```
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
    $ vimenv install v7.4.169
  5. if you want to apply patch, please edit ~/.vimenv/share/p1_patches.
     you must write the urls of patch file on p1_patches.
    $ mkdir ~/.vimenv/share
    $ vim ~/.vimenv/share/p1_patches
    $ vimenv install v7.4.169
  6. if you want to set variables, please edit ~/.vimenv/share/setenv
    $ mkdir ~/.vimenv/share
    $ vim ~/.vimenv/share/setenv
    $ vimenv install v7.4.169
```

# DESCRIPTION

  vim-build is an [vimenv](https://github.com/raa0121/vimenv) plugin that
  provides an `vimenv install` command to compile and install latest version
  of vim on Unix-like systems.
