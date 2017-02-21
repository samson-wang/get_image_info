# get_image_info
Very fast tools to get image information

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
