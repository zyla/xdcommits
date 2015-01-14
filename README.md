# ty janie commicie capturowany xD

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

    # Write the hook yourself because I'm too lazy
    # ...
    git commit

## Copyright issues

`Impact.ttf` is stolen from lolcommits, and I'm too lazy to read the licenses.
