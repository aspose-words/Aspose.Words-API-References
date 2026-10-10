---
title: DocSaveOptions.save_picture_bullet property
linktitle: save_picture_bullet property
articleTitle: save_picture_bullet property
second_title: Aspose.Words for Python
description: "DocSaveOptions.save_picture_bullet property. When ``False``, PictureBullet data is not saved to output document"
type: docs
weight: 60
url: /zh/python-net/aspose.words.saving/docsaveoptions/save_picture_bullet/
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
# 某些文字处理器，如 Microsoft Word 97，与 PictureBullet 数据不兼容。
# 通过在 SaveOptions 对象中设置标志，
# 我们可以在保存时将所有图像项目符号转换为普通项目符号。
save_options = aw.saving.DocSaveOptions(aw.SaveFormat.DOC)
save_options.save_picture_bullet = False
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.PictureBullets.doc', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

