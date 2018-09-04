# ComputationalGenomicsManual

Robs manual for the computational genomics and bioinformatics class

# About this manual

Rob, Liz Dinsdale, Tom Jeffries, Bruno Gomez-Gil, and several other colleagues and friends have been teaching genomics and metagenomics for a long time. They have written this manual over the course of several years, and in a variety of formats. Rob moved it to markdown using GitHub in Fall 2018 as part of his computational genomics class.

You can view this manual online at https://linsalrob.github.io/ComputationalGenomicsManual/.

# Companion Videos

Companion videos that accompany this class are available on You Tube on [Rob's YouTube Playlist](https://www.youtube.com/playlist?list=PLpPXw4zFa0uLMHwSZ7DMeLGjIUgo1IBbn).

# Chapter Index

1. [Linux](Linux/)
2. [Sequencing Overview](Sequencing/)
3. [Sequence File Formats](SequenceFileFormats/)
4. [Sequence Quality Control](SequenceQC/)
5. [Whole Genome Sequencing](Whole_Genome_Sequencing)

# Creating PDFs

In each directory we include PDFs of the current state of the README. These are made with pandoc, and you can recreate the PDF at any time using the command (of course, chaning FILE to the appropriate name):

```
pandoc README.md -f markdown --latex-engine=xelatex --columns 100 --smart -s -o FILE.pdf
```

or for all directories:

```
for DIR in $(find -maxdepth 1 -type d | sed -e 's/.\/\..*//; s/^\.$//; s/\.\///'); do
	echo $DIR
	cd $DIR
	pandoc README.md -f markdown --latex-engine=xelatex --columns 100 --smart -s -o $DIR.pdf
	cd ../
done
```

# About Copyright Information

Some of the images used in this manual are currently copyright other people. As noted above, Rob and friends wrote this manual over many years and added the images and cartoons to lighten the manual. We are in the process of identifying the copyright holders and/or identifying images that are not copyrighted. If your rights have been infringed upon, if you would like to provide an indemnification, or if you would like to provide a non-copyrighted image, please contact Rob.

# Copyright

This manual is Copyright Robert A. Edwards.

# Citation

If you wish to cite this manual, please cite: *Edwards, R. 2018. Computational Genomics. https://linsalrob.github.io/ComputationalGenomicsManual/. Accessed [today's date]*
