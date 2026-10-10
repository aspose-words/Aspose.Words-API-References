---
title: RtfSaveOptions.export_compact_size property
linktitle: export_compact_size property
articleTitle: export_compact_size property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.export_compact_size property. Allows to make output RTF documents smaller in size, but if they contain  RTL (right-to-left) text, it will not be displayed correctly."
type: docs
weight: 20
url: /sv/python-net/aspose.words.saving/rtfsaveoptions/export_compact_size/
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
# Skapa ett "RtfSaveOptions"-objekt för att skicka till dokumentets "Save"-metod för att ändra hur vi sparar det till en RTF.
options = aw.saving.RtfSaveOptions()
self.assertEqual(aw.SaveFormat.RTF, options.save_format)
# Ställ in egenskapen "ExportCompactSize" till "true" för att
# minska den sparade dokumentets storlek på bekostnad av kompatibilitet med höger‑till‑vänster‑text.
options.export_compact_size = True
# Ställ in egenskapen "ExportImagesFotOldReaders" till "true" för att använda extra nyckelord för att säkerställa att vårt dokument är
# kompatibelt med läsare före Microsoft Word 97 och WordPad.
# Ställ in egenskapen "ExportImagesFotOldReaders" till "false" för att minska dokumentets storlek,
# men förhindra gamla läsare från att kunna läsa några icke‑metafil- eller BMP‑bilder som dokumentet kan innehålla.
options.export_images_for_old_readers = export_images_for_old_readers
doc.save(file_name=ARTIFACTS_DIR + 'RtfSaveOptions.ExportImages.rtf', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [RtfSaveOptions](../)

