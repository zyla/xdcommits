Everybody knows that [lolcommits](https://github.com/mroth/lolcommits) is the
most important tool in modern software development. However, not everybody can
be bothered to install 12434 RubyGerms just to shell out to mplayer and
ImageMagick.

Therefore I present you a clone, xdcommits, written in plain bash.

## Requirements

 - mplayer (with video4linux support - not enabled by default in gentoo)
 - ImageMagick

## Installation

Link `xdcommits` binary to a directory in your PATH (Note: if you copy, you must
also copy Impact.ttf).

## Usage

Manual capture:

    xdcommits capture

Automatic capture:

    xdcommits enable
    git commit # should trigger a capture

## Configuration

`xdcommits`' configuration is stored in Git config, in the section `[xdcommits]`.
This gives you ability to have global "default" config, and tweak settings
per-repo.
Relevant options:

 - `xdcommits.targetDir` - where the images will be stored. Repository name is
   always appended to this dir. Default: `~/.lolcommits`, for compatibility.

 - `xdcommits.settleFrames` - number of frames to discard before the real
   capture. Use this is if your webcam takes some time to warm up. Default
   value: 1 (the second frame will be used).
 
 - `xdcommits.gifFrames` - number of frames used when capturing GIFs. Note that
   `settleFrames` is also respected; GIF frames will be captured after the
   initial discarded frames.
 
 - `xdcommits.imageViewer` - command used by `xdcommits show`. One argument will
   be passed - the image file name.
 
 - `xdcommits.application` - used to specify which capture application should be
   used. Current options are `ffmpeg` and `mplayer`. The default is `mplayer`.

## Copyright issues

`Impact.ttf` is stolen from lolcommits, and I'm too lazy to read the licenses.
