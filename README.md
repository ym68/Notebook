# Hello-world
Hello world testing
This is the change to Hello-world by ym68 in May 2016

### piexif
from PIL import Image
import piexif

im = Image.open(filename)
exif_dict = piexif.load(im.info["exif"])
#### process im and exif_dict...
w, h = im.size
exif_dict["0th"][piexif.ImageIFD.XResolution] = (w, 1)
exif_dict["0th"][piexif.ImageIFD.YResolution] = (h, 1)
exif_bytes = piexif.dump(exif_dict)
im.save(new_file, "jpeg", exif=exif_bytes)
