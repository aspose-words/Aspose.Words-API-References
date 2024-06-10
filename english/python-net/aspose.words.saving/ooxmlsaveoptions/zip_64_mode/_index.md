---
title: OoxmlSaveOptions.zip_64_mode property
linktitle: zip_64_mode property
articleTitle: zip_64_mode property
second_title: Aspose.Words for Python
description: "OoxmlSaveOptions.zip_64_mode property. Specifies whether or not to use ZIP64 format extensions for the output document"
type: docs
weight: 80
url: /python-net/aspose.words.saving/ooxmlsaveoptions/zip_64_mode/
---

## OoxmlSaveOptions.zip_64_mode property

Specifies whether or not to use ZIP64 format extensions for the output document.
The default value is [Zip64Mode.NEVER](../../zip64mode/#NEVER).



```python
@property
def zip_64_mode(self) -> aspose.words.saving.Zip64Mode:
    ...

@zip_64_mode.setter
def zip_64_mode(self, value: aspose.words.saving.Zip64Mode):
    ...

```

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

* module [aspose.words.saving](../../)
* class [OoxmlSaveOptions](../)
* property [OoxmlSaveOptions.zip_64_mode](./)

