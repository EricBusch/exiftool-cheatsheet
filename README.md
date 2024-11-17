# exiftool Cheat Sheet
These are useful commands for dealing with EXIF data for still images using the [EXIFTool](https://exiftool.org/) command line tool.

### Remove Ratings & Keywords

```bash
exiftool -Rating= -Good= -Pick= -Keywords= -Subject= -WeightedFlatSubject= a.jpg
```

### Remove Date Image was Created

```bash
exiftool -DateTimeOriginal= -CreateDate= -DigitalCreationDate= -DigitalCreationTime= -DateCreated= -SubSecCreateDate= -SubSecDateTimeOriginal= -DigitalCreationDateTime=
```
