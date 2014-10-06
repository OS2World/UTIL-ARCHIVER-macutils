This archive contains several compiled utilies for use in OS/2.
They were comiled with the EMX/GCC compiler, and you *MUST* have the
files  EMX.DLL, EMXLIBC.DLL, and EMXIO.DLL (version 0.8e or higher)
These can be found the in the DLL directory of this archive.
The DLLs must be installed in a directory that is listed
in the LIBPATH entry in config.sys.


These utilities are for using MacIntosh files and archives under OS/2.
Compiled by John Paul Morrison (jmorriso@ee.ubc.ca)

Source code is available seperately.

binhex, hexbin, macsave, macstream, macunpack:
        written by Dik Winter (dik@cwi.nl)

unpost
        written by I. Lee Hetherington (ilh@lcs.mit.edu)
        unpost is part of a larger package, but only unpost relates to
        the Mac. (unpost is part of t1utils, also available on ftp-os2)

I haven't tested these programs that thoroughly, but macunpack, binhex and
hexbin seam to work. Send me e-mail if anything seams strange, or contact
the original author (although they won't know anything about the OS/2 port).

Quick Tip:
        these utils can be used to unpack fonts for the MacIntosh. Mac Fonts
        are very commonly available for copying, and the Mac ones are
        usually better quality.

        .hqx files need to be converted with hexbin

        .sit, .cpt etc need to be unpacked with macunpack
            use macunpack -3 file     to unpack, as this will split
            up the Mac info and resource forks, from the useful data.

            if you want to get Adobe Type 1 fonts working, use
            unpost -br font.rsrc font.pfb to make a .pfb file useable
            under OS/2.
            The font.afm.data should be useable under OS/2 without
            more conversion. (?) Anyway, the AFM is a text file, and
            macunpack -3u ... when extracting the AFM file will convert
            it to UNIX text format; you can use your own utils to convert
            the UNIX format into OS/2 text format.

            You should then make sure you have font.afm and font.pfb
            (rename if needed) and then you can install the fonts under
            OS/2. I've converted several Mac Type 1 fonts, and I got them
            working fine.


BUGS:
        I have made NO attempt whatsoever to support the MSDOS/FAT 8.3
        filename format. If you don't like that, get the source code and
        change it. Anyone with OS/2 should have at least one HPFS partition
        anyway.

        There is no option to convert Mac text files into OS/2 text files.
        There is an option to convert Mac text files into UNIX text files.
        Maybe I'll add the feature, or bug the author to add that later.



