## WHY?

Because I want to **upload audio files to YouTube**.

To be able to do that I must first [convert audio files into a format that will work on YouTube] [1] and I want to do that through GNU/Linux command-line.

## WHAT?

This bash shell wrapper script will take **audio file as input** and **output video file** ready for upload to YouTube (e.g., via command-line script [youtube-upload](https://code.google.com/p/youtube-upload/ "youtube-upload")).

Audio formats supported: MP2, MP3, LC-AAC, HE-AAC, AC3

Audio quality remains unchanged therefore output file will be slightly bigger than input file.

## HOW?

### USAGE

    $ encode4yt input

Output file will be written in the same directory where input file is located and also will have identical name, only different extension (i.e., **.mp4**).

### REQUIREMENTS

1. [GNU sed](http://www.gnu.org/software/sed/ "GNU sed")
2. [ImageMagick](http://www.imagemagick.org/ "ImageMagick")
3. [FFmpeg](http://ffmpeg.org/ "FFmpeg")

### INSTALLATION

Example commands are based on Ubuntu 12.04 LTS.

0. Install requirements, e.g.:
    $ sudo apt-get install sed imagemagick ffmpeg
1. Download and uncompress EncodeForYouTube, e.g.:
    $ sudo wget -q https://github.com/mariomaric/EncodeForYouTube/archive/master.tar.gz -O - | tar -C /opt -xz
2. Create a symbolic link to the `encode4yt.sh` in a directory that is already in your PATH, e.g.:
    $ sudo ln -s /opt/EncodeForYouTube-master/encode4yt.sh /usr/local/bin/encode4yt

## MISCELLANEOUS

This script is based on various sources from Internet, mostly from:

- [EncodeforYouTube FFmpeg wiki page](https://trac.ffmpeg.org/wiki/EncodeforYouTube "How to Encode Videos for YouTube and other Video Sharing Sites")
- [FFmpeg documentation](http://ffmpeg.org/ffmpeg-all.html "FFmpeg documentation")
- [ImageMagick v6 Examples -- Text to Image Handling](http://www.imagemagick.org/Usage/text/ "ImageMagick v6 Examples -- Text to Image Handling")
- [Advanced encoding settings](https://support.google.com/youtube/answer/1722171?hl=en&ref_topic=2888648 "Advanced encoding settings @ YouTube upload instructions and settings help")

[1]: https://support.google.com/youtube/answer/1696878?hl=en&ref_topic=2888648
    "Upload audio or image files @ YouTube upload instructions and settings help"
