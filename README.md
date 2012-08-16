If you have used the code from [Initializr](http://www.initializr.com),
you may have noticed that some of the files have DOS-style line endings (CR+LF)
instead of Unix-style line endings (LF).
See the Initializr bug report
[All output files should have Unix-style line-endings][1].

This is annoying to no end because once you notice it,
you may already have committed and made changes to the code.
Changing the code then may cause conflicts in your version control.

Another issue is that Initializr's code mixes tabs and spaces,
and some files have lines ending with spaces.

This little script fixes these problems.

To avoid version conflicts, make sure you run this command directly after
unpacking the zip file you get from Initializr.

Just `cd` to the directory where you extracted the zip file from Initializr
and run:

    initializr-cleanup

This script requires the commands `dos2unix`, `sed` and `expand`.
I have only tested it on Linux,
so please let me know if it works or not on Macs.

[1]: https://github.com/verekia/initializr/issues/40
