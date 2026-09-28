---
title: DocSaveOptions.save_picture_bullet property
linktitle: save_picture_bullet property
articleTitle: save_picture_bullet property
second_title: Aspose.Words for Python
description: "DocSaveOptions.save_picture_bullet property. When ``False``, PictureBullet data is not saved to output document"
type: docs
weight: 60
url: /de/python-net/aspose.words.saving/docsaveoptions/save_picture_bullet/
---

## DocSaveOptions.save_picture_bullet property

When ``False``, PictureBullet data is not saved to output document.
Default value is ``True``.



```python
@property
def save_picture_bullet(self) -> bool:
    ...

@save_picture_bullet.setter
def save_picture_bullet(self, value: bool):
    ...

```

### Remarks

This option is provided for Word 97, which cannot work correctly with PictureBullet data.
To remove PictureBullet data, set the option to "false".




### Examples

Shows how to omit PictureBullet data from the document when saving.

```python
doc = aw.Document(file_name=MY_DIR + 'Image bullet points.docx')
# Einige Textverarbeitungsprogramme, wie Microsoft Word 97, sind mit PictureBullet-Daten nicht kompatibel.
# Durch das Setzen eines Flags im SaveOptions-Objekt,
# können wir beim Speichern alle Bild‑Aufzählungszeichen in normale Aufzählungszeichen umwandeln.
save_options = aw.saving.DocSaveOptions(aw.SaveFormat.DOC)
save_options.save_picture_bullet = False
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.PictureBullets.doc', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

