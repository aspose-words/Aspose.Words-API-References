---
title: RtfSaveOptions.export_compact_size property
linktitle: export_compact_size property
articleTitle: export_compact_size property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.export_compact_size property. Allows to make output RTF documents smaller in size, but if they contain  RTL (right-to-left) text, it will not be displayed correctly."
type: docs
weight: 20
url: /tr/python-net/aspose.words.saving/rtfsaveoptions/export_compact_size/
---

## RtfSaveOptions.export_compact_size property

Allows to make output RTF documents smaller in size, but if they contain 
RTL (right-to-left) text, it will not be displayed correctly.

Default value is ``False``.



```python
@property
def export_compact_size(self) -> bool:
    ...

@export_compact_size.setter
def export_compact_size(self, value: bool):
    ...

```

### Remarks

If the document that you want to convert to RTF using Aspose.Words does not contain
right-to-left text in languages like Arabic, then you can set this option to ``True``
to reduce the size of the resulting RTF.




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

