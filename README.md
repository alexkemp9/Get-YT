# Get-YT
A BASH Script to Download mp4, poster-image + captions for YT videos

## *Basics*
This script file is designed for use by any-user (no root access required) within a Terminal. It’s principal purpose is to make it easy & reliable to download video, poster + captions for a desired YT video. It has been used under *Devuan* (a systemD-free version of *Debian*). In addition to BASH, the main utilities required are common items such as FFMPEG & TOUCH + the uncommon item YAD (*“Yet Another Dialog”*, described as a *“tool for creating graphical dialogs from shell scripts”*) + FIREFOX.

The main item to change is line 64 (change to a suitable directory):

```bash
if [[ ! "$DIR" ]]
then
   DIR="$HOME/Your/Dir"
fi

```
## *Extra*
The script interchanges between command-line & a YAD dialog. This dialog is vital in the 2nd part in choosing the precise variant of video to download.

## *Begin*
The following will assume that you have created a dir `~/.local/sbin` within which you store the bash-file; this is to set the script as executable for current user only:

```bash
$ chmod 0700 ~/.local/sbin/getYT
$ la ~/.local/sbin/getYT
-rwx------ 1 user user 17461 14783 Apr  6  2022 /home/user/.local/sbin/getYT
```
If the file is opened without any parameters, this is the dialog that you will see:

![dialog1](https://github.com/alexkemp9/Get-YT/blob/main/Screenshot_2023-05-30_17-17-20.png)

(you forgot to change line#64, did you not?)

Choosing now one of my videos (at https://youtu.be/9RLe2vDv6s0, unfortunately very low resolution screen), filling in the blanks & pressing ‘OK’ gives the second dialog:

![dialog2](https://github.com/alexkemp9/Get-YT/blob/main/Screenshot_2023-05-30_17-40-17.png)

That has tick-boxes to the left of the screen. To get Audio tick the m4a line, then choose the video resolution that you want, and when complete press ‘OK’. The Audio (if chosen) + video files will be downloaded then combined. Next will be the best-res poster and then captions. It could be scores & scores of files, so choose a single directory
.
