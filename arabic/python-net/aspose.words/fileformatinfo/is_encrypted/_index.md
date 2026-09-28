---
title: FileFormatInfo.is_encrypted property
linktitle: is_encrypted property
articleTitle: is_encrypted property
second_title: Aspose.Words for Python
description: "FileFormatInfo.is_encrypted property. Returns ``True`` if the document is encrypted and requires a password to open."
type: docs
weight: 40
url: /ar/python-net/aspose.words/fileformatinfo/is_encrypted/
---

## FileFormatInfo.is_encrypted property

Returns ``True`` if the document is encrypted and requires a password to open.



```python
@property
def is_encrypted(self) -> bool:
    ...

```

### Remarks

This property exists to help you sort documents that are encrypted from those that are not.
If you attempt to load an encrypted document using Aspose.Words without supplying a password an
exception will be thrown. You can use this property to detect whether a document requires a password
and take some action before loading a document, for example, prompt the user for a password.




### Examples

Shows how to use the FileFormatUtil class to detect the document format and encryption.

```python
doc = aw.Document()
# قم بتكوين كائن SaveOptions لتشفير المستند
# مع كلمة مرور عند حفظه، ثم احفظ المستند.
save_options = aw.saving.OdtSaveOptions(save_format=aw.SaveFormat.ODT)
save_options.password = 'MyPassword'
doc.save(file_name=ARTIFACTS_DIR + 'File.DetectDocumentEncryption.odt', save_options=save_options)
# تحقق من نوع ملف مستندنا، وحالة تشفيره.
info = aw.FileFormatUtil.detect_file_format(file_name=ARTIFACTS_DIR + 'File.DetectDocumentEncryption.odt')
self.assertEqual('.odt', aw.FileFormatUtil.load_format_to_extension(info.load_format))
self.assertTrue(info.is_encrypted)
```

### See Also

* module [aspose.words](../../)
* class [FileFormatInfo](../)
* property [FileFormatInfo.load_format](../load_format/)

