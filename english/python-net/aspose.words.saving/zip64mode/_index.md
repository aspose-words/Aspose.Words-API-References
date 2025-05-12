---
title: Zip64Mode enumeration
linktitle: Zip64Mode enumeration
articleTitle: Zip64Mode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.saving.Zip64Mode enumeration. Specifies when to use ZIP64 format extensions for OOXML files."
type: docs
weight: 960
url: /python-net/aspose.words.saving/zip64mode/
---

## Zip64Mode enumeration

Specifies when to use ZIP64 format extensions for OOXML files.

OOXML file is a ZIP-archive that has a 4 GB (2^32 bytes) limit on uncompressed size of a file,
compressed size of a file, and total size of the archive, as well as a limit of 65,535 (2^16-1) files in archive.
ZIP64 format extensions increase the limits to 2^64.


### Members

| Name | Description |
| --- | --- |
| NEVER | Do not use ZIP64 format extensions. |
| IF_NECESSARY | If necessary use ZIP64 format extensions. |
| ALWAYS | Always use ZIP64 format extensions. |

### Examples

Shows how to use ZIP64 format extensions.

```python
builder = aw.DocumentBuilder()
for i in range(0, 10000):
    bmp = aspose.pydrawing.Bitmap(5, 5)
    g = aspose.pydrawing.Graphics.from_image(bmp)
    g.clear(aspose.pydrawing.Color.from_argb(random.randint(0, 254), random.randint(0, 254), random.randint(0, 254)))
    data = io.BytesIO()
    bmp.save(data, aspose.pydrawing.imaging.ImageFormat.bmp)
    builder.insert_image(data)
    data.close()
options = aw.saving.OoxmlSaveOptions()
options.zip_64_mode = aw.saving.Zip64Mode.ALWAYS
builder.document.save(ARTIFACTS_DIR + 'OoxmlSaveOptions.Zip64ModeOption.docx')
```

### See Also

* module [aspose.words.saving](../)
* property [OoxmlSaveOptions.zip_64_mode](../ooxmlsaveoptions/zip_64_mode/)

