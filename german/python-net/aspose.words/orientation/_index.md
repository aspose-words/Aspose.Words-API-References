---
title: Orientation enumeration
linktitle: Orientation enumeration
articleTitle: Orientation enumeration
second_title: Aspose.Words for Python
description: "aspose.words.Orientation enumeration. Specifies page orientation."
type: docs
weight: 880
url: /de/python-net/aspose.words/orientation/
---

## Orientation enumeration

Specifies page orientation.


### Members

| Name | Description |
| --- | --- |
| PORTRAIT | Portrait page orientation (narrow and tall). |
| LANDSCAPE | Landscape page orientation (wide and short). |

### Examples

Shows how to apply and revert page setup settings to sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ändern Sie die Seiteneinrichtungseigenschaften für den aktuellen Abschnitt des Builders und fügen Sie Text hinzu.
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.vertical_alignment = aw.PageVerticalAlignment.CENTER
builder.writeln('This is the first section, which landscape oriented with vertically centered text.')
# Wenn wir einen neuen Abschnitt mit einem Document Builder starten,
# erbt er die aktuellen Seiteneinrichtungseigenschaften des Builders.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(aw.Orientation.LANDSCAPE, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.CENTER, doc.sections[1].page_setup.vertical_alignment)
# Wir können seine Seiteneinrichtungseigenschaften mit der Methode "ClearFormatting" auf ihre Standardwerte zurücksetzen.
builder.page_setup.clear_formatting()
self.assertEqual(aw.Orientation.PORTRAIT, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.TOP, doc.sections[1].page_setup.vertical_alignment)
builder.writeln('This is the second section, which is in default Letter paper size, portrait orientation and top alignment.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.ClearFormatting.docx')
```

### See Also

* module [aspose.words](../)

