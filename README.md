## Overview

We found ourselves in a situation where we scanned a number of pictures.
However, these pictures were scanned as PDF documents, meaning there were
single or multiple nested JPG files inside each PDF.  That wasn't what we
wanted, so we needed a quick tool to convert this.

They all had spaces in them, so it can handle spaces anywhere in parameters
without issue.

## Requirements

- Requires [`pdfimages`](https://en.wikipedia.org/wiki/Pdfimages) to be globally executable
- Requires `/bin/bash` to be a BASH shell.

## Usage

    ./pdf2jpg-converter list_of_pdf_files_to_parse

## Quirks

When these were scanned in, multiple images in one PDF was scanned like "blah
x2.pdf".  I wanted to strip off "x2" since that was just saying that there were
two images in the file.  If you don't want that, the source is pretty clear on
how that works.

The completed files are dumped in `./completed`.  If you want this to go
somewhere else, just edit the environment variable in the file.

## License

`pdf_converter` is implemented according to the BSD 3-Clause License.  You can
find a copy in the LICENSE file.
