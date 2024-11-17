# exiftool Cheat Sheet
These are useful commands for dealing with EXIF data for still images using the [https://exiftool.org/](EXIF Tool) command line tool.

### Remove Ratings & Keywords

```bash
exiftool -Rating= -Good= -Pick= -Keywords= -Subject= -WeightedFlatSubject= a.jpg
```
