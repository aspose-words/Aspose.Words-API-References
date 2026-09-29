---
title: RtfSaveOptions.export_images_for_old_readers property
linktitle: export_images_for_old_readers property
articleTitle: export_images_for_old_readers property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.export_images_for_old_readers property. Specifies whether the keywords for old readers are written to RTF or not"
type: docs
weight: 30
url: /ru/python-net/aspose.words.saving/rtfsaveoptions/export_images_for_old_readers/
---

## RtfSaveOptions.export_images_for_old_readers property

Specifies whether the keywords for "old readers" are written to RTF or not.
This can significantly affect the size of the RTF document.

Default value is ``True``.



```python
@property
def export_images_for_old_readers(self) -> bool:
    ...

@export_images_for_old_readers.setter
def export_images_for_old_readers(self, value: bool):
    ...

```

### Remarks

"Old readers" are pre-Microsoft Word 97 applications and also WordPad.
When this option is ``True`` Aspose.Words writes additional RTF keywords.
These keywords allow the document to be displayed correctly when opened in an 
"old reader" application, but can significantly increase the size of the document.

If you set this option to ``False``, then only images in WMF, EMF and BMP formats
will be displayed in "old readers".




### Examples

Shows how to save a document to .rtf with custom options.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
# Создайте объект "RtfSaveOptions", чтобы передать его в метод "Save" документа и изменить способ сохранения в RTF.
options = aw.saving.RtfSaveOptions()
self.assertEqual(aw.SaveFormat.RTF, options.save_format)
# Установите свойство "ExportCompactSize" в "true", чтобы
# уменьшить размер сохраняемого документа ценой совместимости с текстом справа налево.
options.export_compact_size = True
# Установите свойство "ExportImagesFotOldReaders" в "true", чтобы использовать дополнительные ключевые слова и гарантировать, что наш документ
# совместим с читателями предшествующими Microsoft Word 97 и WordPad.
# Установите свойство "ExportImagesFotOldReaders" в "false", чтобы уменьшить размер документа,
# но предотвратить возможность старым читателям читать любые изображения, не являющиеся метафайлами или BMP, которые могут быть в документе.
options.export_images_for_old_readers = export_images_for_old_readers
doc.save(file_name=ARTIFACTS_DIR + 'RtfSaveOptions.ExportImages.rtf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [RtfSaveOptions](../)

