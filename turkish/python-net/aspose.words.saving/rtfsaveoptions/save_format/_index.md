---
title: RtfSaveOptions.save_format property
linktitle: save_format property
articleTitle: save_format property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.save_format property. Specifies the format in which the document will be saved if this save options object is used"
type: docs
weight: 40
url: /tr/python-net/aspose.words.saving/rtfsaveoptions/save_format/
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
# "RtfSaveOptions" nesnesi oluşturun ve belge'nin "Save" yöntemine geçirin, RTF olarak nasıl kaydedeceğimizi değiştirmek için.
options = aw.saving.RtfSaveOptions()
self.assertEqual(aw.SaveFormat.RTF, options.save_format)
# "ExportCompactSize" özelliğini "true" olarak ayarlayın,
# kaydedilen belgenin boyutunu, sağdan sola metin uyumluluğu pahasına azaltmak için.
options.export_compact_size = True
# "ExportImagesFotOldReaders" özelliğini "true" olarak ayarlayın, ek anahtar kelimeler kullanarak belgemizin
# Microsoft Word 97 öncesi okuyucular ve WordPad ile uyumlu olmasını sağlamak için.
# "ExportImagesFotOldReaders" özelliğini "false" olarak ayarlayın, belgenin boyutunu azaltmak için,
# ancak eski okuyucuların belge içinde bulunabilecek metafile olmayan veya BMP resimlerini okuyabilmesini engellemek için.
options.export_images_for_old_readers = export_images_for_old_readers
doc.save(file_name=ARTIFACTS_DIR + 'RtfSaveOptions.ExportImages.rtf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [RtfSaveOptions](../)

