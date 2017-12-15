# get_image_info
Very fast tools to get image information.

The PIL, opencv and other libs are too heavy to deal with simple tasks, such as get image format, width and height. They usally read whole picture into memory and decode it which is wasty.

Such imformation is stored in the first dozens of bytes in the file. So just read and parse them and get what you want. All the work can be done exteemly faster than those libs.

Besides, when useing python deal with iamges, the files could be already in the memory, e.g. downloaded from web, the tool can deal with it by providing a file like object which has `read()` method.

Pythonic image processing often composed of pipelines, for resize, crop, rotate, scale and other work, a [py-jpegtran](https://github.com/samson-wang/jpegtran-cffi) is recommended.

- get image type, width and height

```
# Input is a file or StringIO object
# Return tuple (image_type, width, height)
# Only support 'gif/jpeg/png'
get_image_info(pic)
```

- Verify if an image is 'JPEG' format

```
# Input is a file or StringIO object
# Return bool
pic = open('path/pic')
# import StringIO
# pic = StringIO(data)
verify_jpeg(pic)
```
