# Parse Engine Data


This repo is for parsing files in the [.NORM format](https://xkcd.com/2116/) to
csv.


## Parsing an image

To parse images I've been using
[PlotDigitizer](https://github.com/dilawar/PlotDigitizer/).

``` sh
python3 -m venv env
source env/bin/activate
pip install plotdigitizer
```

Now you should have access to the `plotdigitizer` command.

To prepare the images you have to crop them to just the actual graph, no numbers
or anything else. I use GIMP for this. PlotDigitizer also only supports one
line, it doesn't support multiple lines in different colors. To get around this
I make two copies of the image, then erase one of the lines in each image, using
GIMP. Then PlotDigitizer can do its thing.
