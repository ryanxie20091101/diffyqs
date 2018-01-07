Notes on Diffy Qs: Differential Equations for Engineers
-------------------------------------------------------

A free online textbook.  See http://www.jirka.org/diffyqs/

* diffyqs.tex is the main file, no real content here, that's in the chapter files
* ch-???.tex are the files with the content of the various chapters
* diffyqssetup.sty is the preamble for the PDF version
* diffyqssetup-tex4ht.sty is the preamble for creating the web version with tex4ht, but this is unlikely to work for anyone but me at the moment.  Also note that the google tracking code for my website is here, so if you want to use this you should change that first.

Figures are in figures/

Note: Some of the shell(.sh) and Perl(.pl) scripts here are really for me and are really hacky ways to just do things.  Most of them are for generating the web version.  Feel free to ignore them.

* convert-to-mbx.??: is work in progress conversion script to PreTeXt (used to be MathBookXML or MBX) for a better looking online version.  The output is not plain PreTeXt, it contains custom elements.  The script to run is convert-to-mbx.sh, which is a shell script.  This runs convert-to-mbx.pl which actually does the conversion, then it runs xsltproc on the result.  The result is stored in html subdirectory (old one is moved out of the way).  Some svg and png figures are created in the process, they can be optimized by optimize-svgs.sh (uses svgo which you might have to install).  Currently uses the svgs, which are for the most part more optimal size-wise, but only if svgo is run on them.  Also notice that svgo currently clobbers someof the more complicated ones without disabeling one of the plugins, so best to check the output for correctness.
* diffyqs-html.xsl: The xsl to use to convert the PreTeXt output.

The tex sources require a very recent LaTeX, if your latex does not have a recent enough ocgx2 package, you can simply comment out that line in
diffyqssetup.sty.
