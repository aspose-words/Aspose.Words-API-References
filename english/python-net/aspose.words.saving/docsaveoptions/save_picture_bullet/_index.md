---
title: DocSaveOptions.save_picture_bullet property
linktitle: save_picture_bullet property
articleTitle: save_picture_bullet property
second_title: Aspose.Words for Python
description: "DocSaveOptions.save_picture_bullet property. When ``False``, PictureBullet data is not saved to output document"
type: docs
weight: 50
url: /python-net/aspose.words.saving/docsaveoptions/save_picture_bullet/
---

## DocSaveOptions.save_picture_bullet property

When ``False``, PictureBullet data is not saved to output document.
Default value is ``True``.


This option is provided for Word 97, which cannot work correctly with PictureBullet data. 
To remove PictureBullet data, set the option to "false".




### Examples

Shows how to omit PictureBullet data from the document when saving.

```python
doc = aw.Document(MY_DIR + "Image bullet points.docx")

# Some word processors, such as Microsoft Word 97, are incompatible with PictureBullet data.
# By setting a flag in the SaveOptions object,
# we can convert all image bullet points to ordinary bullet points while saving.
save_options = aw.saving.DocSaveOptions(aw.SaveFormat.DOC)
save_options.save_picture_bullet = False

doc.save(ARTIFACTS_DIR + "DocSaveOptions.picture_bullets.doc", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

