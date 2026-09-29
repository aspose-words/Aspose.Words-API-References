---
title: RtfSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 40
url: /ru/python-net/aspose.words.saving/rtfsaveoptions/save_format/
---

## RtfSaveOptions.save_format property

Specifies the format in which the document will be saved if this save options object is used.
Can only be [SaveFormat.RTF](../../../aspose.words/saveformat/#RTF).



```python
@property
def save_format(self) -> aspose.words.SaveFormat:
    ...

@save_format.setter
def save_format(self, value: aspose.words.SaveFormat):
    ...

```

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

