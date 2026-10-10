---
title: PageVerticalAlignment enumeration
linktitle: PageVerticalAlignment enumeration
articleTitle: PageVerticalAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.PageVerticalAlignment enumeration. Specifies vertical justification of text on each page."
type: docs
weight: 940
url: /fr/python-net/aspose.words/pageverticalalignment/
---

## PageVerticalAlignment enumeration

Specifies vertical justification of text on each page.


### Members

| Name | Description |
| --- | --- |
| BOTTOM | Text is aligned at the bottom of the page. |
| CENTER | Text is aligned in the middle of the page. |
| JUSTIFY | Text is spread to fill the page. |
| TOP | Text is aligned at the top of the page. |

### Examples

Shows how to apply and revert page setup settings to sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Modifiez les propriétés de mise en page pour la section actuelle du constructeur et ajoutez du texte.
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.vertical_alignment = aw.PageVerticalAlignment.CENTER
builder.writeln('This is the first section, which landscape oriented with vertically centered text.')
# Si nous démarrons une nouvelle section en utilisant un constructeur de document,
# elle héritera des propriétés de mise en page actuelles du constructeur.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(aw.Orientation.LANDSCAPE, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.CENTER, doc.sections[1].page_setup.vertical_alignment)
# Nous pouvons rétablir ses propriétés de mise en page à leurs valeurs par défaut en utilisant la méthode "ClearFormatting".
builder.page_setup.clear_formatting()
self.assertEqual(aw.Orientation.PORTRAIT, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.TOP, doc.sections[1].page_setup.vertical_alignment)
builder.writeln('This is the second section, which is in default Letter paper size, portrait orientation and top alignment.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.ClearFormatting.docx')
```

### See Also

* module [aspose.words](../)
* class [PageSetup](../pagesetup/)
* property [PageSetup.vertical_alignment](../pagesetup/vertical_alignment/)

