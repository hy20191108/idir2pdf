idir2pdf (image dir to pdf)
=======
This library convert zip file containing image file to pdf file.
- fast convert
- pdf page width is same
- This library convert on memory, not use tmp folder.

Support image format in zip
- jpeg, jpeg2000, png,  webp, avif, heif, psd, tiff, etc.

Usage
-----

	$ idir2pdf sample1.zip
    $ idir2pdf sample2.zip sample3.zip


As result, this library make sample1.pdf sample2.pdf sample3.pdf

In the case of Linux environment, you can use

	$ idir2pdf sample*.zip

Installation
------------

If you want to install, you can run:

	$ pip install idir2pdf

Library
-------

The package can also be used as a library:

```python
import idir2pdf

# usecase 1
idir2pdf.convert("input.zip", "output.pdf")

# usecase 2
with open("input.zip", "rb") as f:
        zip_bin = f.read()
idir2pdf.convert(zip_bin, "output/output2.pdf")

# usecase 3
pdf_bin = idir2pdf.convert("input.zip")
with open("output.pdf", "wb") as f:
    f.write(pdf_bin)

# usecase 4
with open("input.zip", "rb") as f:
    zip_bin = f.read()
pdf_bin = idir2pdf.convert(zip_bin)
with open("output.pdf", "wb") as f:
    f.write(pdf_bin)
```


# Reference
- [img2pdf](https://github.com/myollie/img2pdf)