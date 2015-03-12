ansible-ffmpeg-common
========

Ansible role which installs [ffmpeg](https://ffmpeg.org) using [these](https://trac.ffmpeg.org/wiki/CompilationGuide/Ubuntu) instructions.

Role Variables
--------------
The variables that can be passed to this role and a brief description about
them are as follows.

    # The URL to the ffmpeg sources
    ffmpeg_sources_url: 'http://ffmpeg.org/releases/ffmpeg-snapshot.tar.bz2'

    # The various codec dependencies to install
    ffmpeg_lib_dependencies:
      - libfdk-acc-dev
      - libmp3lame-dev
      - libopus-dev
      - libthoera-dev
      - libvorbis-dev
      - libvpx-dev
      - libx264-dev

    # The configuration flags for the installation
    ffmpeg_configure_flags:
      - '--enable-gpl'
      - '--enable-libass'
      - '--enable-libfdk-aac'
      - '--enable-libfreetype'
      - '--enable-libmp3lame'
      - '--enable-libopus'
      - '--enable-libtheora'
      - '--enable-libvorbis'
      - '--enable-libvpx'
      - '--enable-libx264'
      - '--enable-nonfree'

    # If defined, represents the prefix to use for the installation. Otherwise 
    # the default will be used
    ffmpeg_prefix: '/usr/local'

Example Playbook
-------------------------

1) Install serviio

    - hosts: all
      roles:
      - ansible-ffmpeg-common

Dependencies
------------

None

License
-------

BSD

Author Information
------------------

Parv Mihai