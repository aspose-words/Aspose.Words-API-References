---
title: DocSaveOptions.always_compress_metafiles property
linktitle: always_compress_metafiles property
articleTitle: always_compress_metafiles property
second_title: Aspose.Words for Python
description: "DocSaveOptions.always_compress_metafiles property. When ``False``, small metafiles are not compressed for performance reason"
type: docs
weight: 20
url: /zh/python-net/aspose.words.saving/docsaveoptions/always_compress_metafiles/
---

## DocSaveOptions.always_compress_metafiles property

When ``False``, small metafiles are not compressed for performance reason.
Default value is ``True``, all metafiles are compressed regardless of its size.



```python
@property
def always_compress_metafiles(self) -> bool:
    ...

@always_compress_metafiles.setter
def always_compress_metafiles(self, value: bool):
    ...

```

### Examples

Shows how to change metafiles compression in a document while saving.

```python
# 打开包含 Microsoft Equation 3.0 公式的文档。
doc = aw.Document(file_name=MY_DIR + 'Microsoft equation object.docx')
# 保存文档时，为了性能原因，较小的元文件不会被压缩。
# 我们可以在 SaveOptions 对象中设置标志，以在保存时压缩所有元文件。
# 某些编辑器，如 LibreOffice，无法读取未压缩的元文件。
save_options = aw.saving.DocSaveOptions()
save_options.always_compress_metafiles = compress_all_metafiles
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.AlwaysCompressMetafiles.docx', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

