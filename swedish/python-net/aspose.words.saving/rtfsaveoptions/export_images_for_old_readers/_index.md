---
title: RtfSaveOptions.export_images_for_old_readers property
linktitle: export_images_for_old_readers property
articleTitle: export_images_for_old_readers property
second_title: Aspose.Words for Python
description: "RtfSaveOptions.export_images_for_old_readers property. Specifies whether the keywords for old readers are written to RTF or not"
type: docs
weight: 30
url: /sv/python-net/aspose.words.saving/rtfsaveoptions/export_images_for_old_readers/
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

