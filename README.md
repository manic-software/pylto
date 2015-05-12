# pylto
pylto is a python script which generates a pdf of LTO tape labels for printing onto Avery label sheet 6577

It's a simple program, but it's saved me a bunch of money on professionally generated tape labels; so I thought others might find it useful.

It depends on reportlib for the pdf generation.

Usage: pylto [options] numbers (e.g. 1-5,6,7,8 9-12)
Run without options to launch UI (you'll need the pyqt4 libraries)

Options:
  -h, --help            show this help message and exit
  -g GENERATION, --generation=GENERATION
                        tape generation (defaults to 4)
  -o OFFSET, --offset=OFFSET
                        skip the first 'offset' labels
