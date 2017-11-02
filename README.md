# Welcome to the New Mexico Oil Conservation Division Scraper #

This was written out of frustration for yet another state that sucks at actually
open access oil and gas well data. See, in New Mexico, they give you all the
documents for every well, but they don't label or name any of the documents.
So to get the files you want, you have to do the spray and pray with downloads.
This notebook helps us deal with the ineptitude of the State of New Mexico.

##How do I use this notebook?##

All you need are a few dependencies installed on your machine and the API numbers
for the wells you are interested in. It's written in Python 2.x because some of
the OCR dependencies are not yet ported to Python 3.

##How does it work?##

This notebook downloads the unorganized PDF files to a location on your local
machine, converts them to images, uses optical character recognition (OCR) to
extract text, then classifies the documents using a basic multinomial naive Bayes
classifier. Then we have documents named and we can find what we want faster!

All you need to change is the file paths and the well API numbers to match your
local files and you're all set!

# Dependencies
ImageMagick [http://www.imagemagick.org/script/index.php] external install
Wand [https://pypi.python.org/pypi/Wand] pip install
Python-tesseract [https://pypi.python.org/pypi/pytesseract]
requests, bs4, time, os, re, random, numpy, nltk, autocorrect, scikitlearn
