# Hello-world
Hello world testing
This is the change to Hello-world by ym68 in May 2016


# piexif
### $ pip install piexif

from PIL import Image
impo piexif

im = Image.open(filename)
exif_dict = piexif.load(im.info["exif"])
#### process im and exif_dict...
w, h = im.size
exif_dict["0th"][piexif.ImageIFD.XResolution] = (w, 1)
exif_dict["0th"][piexif.ImageIFD.YResolution] = (h, 1)
exif_bytes = piexif.dump(exif_dict)
im.save(new_file, "jpeg", exif=exif_bytes)

# datetime
import datetime #导入日期时间模块  
today = datetime.date.today() #获得今天的日期  
print(today) #输出今天日期 2017-12-29 datetime  
today = str(today.year)+str(today.month)+str(today.day)  
print(today） #20171229 str  

# time
import time #导入日期时间模块  
today = time.strftime("%Y%m%d") #获得今天的日期 20180101, str   

print(today) #输出今天日期 20171229 str  
