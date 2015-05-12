# pylto
pylto is a python script which generates a pdf of LTO tape labels for printing onto Avery label sheet 6577

A free on-line generator which uses pylto as the back-end is available at [MaNic Software](http://www.manicsoftware.co.uk/pylto).

It's a simple program, but it's saved me a bunch of money on professionally generated tape labels; so I thought others might find it useful.

It depends on reportlib for the pdf generation.

```
Usage: pylto [options] numbers (e.g. 1-5,6,7,8 9-12)
Run without options to launch UI (you'll need the pyqt4 libraries)

Options:
  -h, --help            show this help message and exit
  -g GENERATION, --generation=GENERATION
                        tape generation (defaults to 4)
  -o OFFSET, --offset=OFFSET
                        skip the first 'offset' labels
```

If you have pyqt4 installed and you run without any command line options, you'll get a simple gui.

As input it accepts a numerical range such as 1-20 or 1 2 3 4 5, or 1-20 22 23 25.
Also you can specify the tape generation using -g N.  1 for LTO1, 2 for LTO2 etc etc.
In case you want to finish off a partially used label sheet, use -o N where N is the number of labels you want to skip.

For example to generate labels numbered 1001-1020 for LTO4 tapes:   `pylto -g4 1001-1020 > filename.pdf`
