Polaris CD to Ebook Converter
=============================

Set of scripts to convert HTML sources found on the **Polarisov SF CD-ROM** to
ebook format.

Polaris SF CD-ROM was a publication by Polaris, a publishing company run by
Zoran Živković, containing 227 SF works translated to Serbian, in HTML format.
The second edition was published in 1998.

This project contains scripts which convert the source files from multi-page
HTML to a single-page and fixes broken styles and paragraphs. Then uses the
mighty [Calibre](https://calibre-ebook.com/) to convert to ebooks.

This project does not include the sources, you need to own them yourself.

Usage
-----

Requires python3 and calibre to be installed.

To convert the books to single-page HTML files:

```
python3 polaris_to_html.py <path_to_polaris_cd> <output_directory>
```

The second step is just a wrapper around `ebook-convert` tool which is included
with Calibre. You can just use it directly to convert the books, but I made a
script to simplify the conversion process. It's hardcoded to `mobi` (Kindle)
format.

Once the HTML has been generated, convert the ebooks:

```
python3 html_to_ebook.py "out/*.html"
```

License
-------

The code is licensed under the MIT license.

Copyright 2018 Ivan Habunek

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

