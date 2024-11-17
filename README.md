# exiftool Cheat Sheet
These are useful commands for dealing with EXIF data for still images using the [EXIFTool](https://exiftool.org/) command line tool.

### Remove Ratings & Keywords

```bash
exiftool -Rating= -Good= -Pick= -Keywords= -Subject= -WeightedFlatSubject= a.jpg
```

### Remove Image Creation Date

```bash
exiftool -DateTimeOriginal= -CreateDate= -DigitalCreationDate= -DigitalCreationTime= -DateCreated= -SubSecCreateDate= -SubSecDateTimeOriginal= -HistoryWhen= a.jpg
```

### Set Image Creation Date to File Modified Date

```bash
exiftool -DateTimeOriginal= -CreateDate= -DigitalCreationDate= -DigitalCreationTime= -DateCreated= -SubSecCreateDate= -SubSecDateTimeOriginal= -HistoryWhen= "-DateTimeOriginal<FileModifyDate" "-CreateDate<FileModifyDate" "-DigitalCreationDate<FileModifyDateTime" "-DateCreated<FileModifyDate" "-ModifyDate<FileModifyDate" "-SubSecDateTimeOriginal<FileModifyDate" "-SubSecCreateDate<FileModifyDate" a.jpg
```

### Modify JPGs and Move to New Directory

```bash
exiftool -Rating=  -o /path/to/dest /path/to/src/*.jpg
```

### Put it all together

```bash
exiftool -Rating= -Good= -Pick= -Keywords= -Subject= -WeightedFlatSubject= exiftool -DateTimeOriginal= -CreateDate= -DigitalCreationDate= -DigitalCreationTime= -DateCreated= -SubSecCreateDate= -SubSecDateTimeOriginal= -HistoryWhen= "-DateTimeOriginal<FileModifyDate" "-CreateDate<FileModifyDate" "-DigitalCreationDate<FileModifyDateTime" "-DateCreated<FileModifyDate" "-ModifyDate<FileModifyDate" "-SubSecDateTimeOriginal<FileModifyDate" "-SubSecCreateDate<FileModifyDate" -o /path/to/dest /path/to/src/*.jpg
```
