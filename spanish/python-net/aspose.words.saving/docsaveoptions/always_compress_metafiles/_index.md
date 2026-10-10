---
title: DocSaveOptions.always_compress_metafiles property
linktitle: always_compress_metafiles property
articleTitle: always_compress_metafiles property
second_title: Aspose.Words for Python
description: "DocSaveOptions.always_compress_metafiles property. When ``False``, small metafiles are not compressed for performance reason"
type: docs
weight: 20
url: /es/python-net/aspose.words.saving/docsaveoptions/always_compress_metafiles/
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
# Abra un documento que contenga una fórmula de Microsoft Equation 3.0.
doc = aw.Document(file_name=MY_DIR + 'Microsoft equation object.docx')
# Al guardar un documento, los metafiles más pequeños no se comprimen por razones de rendimiento.
# Podemos establecer una bandera en un objeto SaveOptions para comprimir cada metafile al guardar.
# Algunos editores como LibreOffice no pueden leer metafiles sin comprimir.
save_options = aw.saving.DocSaveOptions()
save_options.always_compress_metafiles = compress_all_metafiles
doc.save(file_name=ARTIFACTS_DIR + 'DocSaveOptions.AlwaysCompressMetafiles.docx', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [DocSaveOptions](../)

