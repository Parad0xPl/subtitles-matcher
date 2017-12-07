# Subtitle Matcher

Simple script for renaming external subtitles matching video files. Designed for
private usage.

## Install

`$ npm install -g subtitles-matcher`

## Usage

`$ match [ options ]`

## How-to use

1. Install script as global with `npm install -g subtitles-matcher`
2. Put all episodes and subtitles for them in directory
3. Open terminal and go to directory
4. Run `match -t` and rate new filenames
5. If you like new names run `match` without test flag

## Options

* -v --video [extension] — Use non-default video extension (Default "mp4")
* -s --subtitles [extension] — Use non-default subtitles extension (Default
  "srt")
* -l --language [code] — Add language code to the subtitles filename
* --skip-season — Skip season number. Usefull when using without sXXeXX
  formatting
* -t --test — Printing new names without moving files
* -h --help — Printing help

## Supported Formats

Scripts ignore video name,

* `s(\d+)e(\d+)` (ex. Sample Show - s99e99.example) as $1 -> season and $2 ->
  episode
* `(\d+) .+` (ex. 01 Sample Show.example) as $1 -> episode
