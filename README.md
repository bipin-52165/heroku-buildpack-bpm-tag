Heroku buildpack: bpm-tag
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for using [bpm-tools](http://www.pogo.org.uk/~mark/bpm-tools/) in your project. 

bpm-tools build is a custom vulcan build downloaded from (http://www.pogo.org.uk/~mark/bpm-tools/releases/bpm-tools-0.3.tar.gz)

It doesn't do anything else, so to actually compile your app you should use [buildpack-bpm-tag](https://github.com/soft-dave/buildpack-bpm-tag) to combine it with a real buildpack.

Usage
-----
To use this buildpack, you should prepare .buildpacks file that contains this buildpack url and your real buildpack url.  

    $ ls
    .buildpacks
    ...
    
    $ cat .buildpacks
    https://github.com/soft-dave/buildpack-bpm-tag

    $ heroku create --buildpack https://github.com/soft-dave/buildpack-bpm-tag

    $ git push heroku master
    ...

You can verify installing ffmpeg by following command.

    $ heroku run "bpm-tag"
