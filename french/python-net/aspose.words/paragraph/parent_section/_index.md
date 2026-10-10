---
title: Paragraph.parent_section property
linktitle: parent_section property
articleTitle: parent_section property
second_title: Aspose.Words for Python
description: "Paragraph.parent_section property. Retrieves the parent [Section](../../section/) of the paragraph."
type: docs
weight: 200
url: /fr/python-net/aspose.words/paragraph/parent_section/
---

## Paragraph.parent_section property

Retrieves the parent [Section](../../section/) of the paragraph.



```python
@property
def parent_section(self) -> aspose.words.Section:
    ...

```

### Examples

Shows how to create a header and a footer.

```python
doc = aw.Document()
# Créez un en-tête et ajoutez-y un paragraphe. Le texte de ce paragraphe
# apparaîtra en haut de chaque page de cette section, au-dessus du texte principal.
header = aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_PRIMARY)
doc.first_section.headers_footers.add(header)
para = header.append_paragraph('My header.')
self.assertTrue(header.is_header)
self.assertTrue(para.is_end_of_header_footer)
# Créez un pied de page et ajoutez-y un paragraphe. Le texte de ce paragraphe
# apparaîtra en bas de chaque page de cette section, sous le texte principal.
footer = aw.HeaderFooter(doc, aw.HeaderFooterType.FOOTER_PRIMARY)
doc.first_section.headers_footers.add(footer)
para = footer.append_paragraph('My footer.')
self.assertFalse(footer.is_header)
self.assertTrue(para.is_end_of_header_footer)
self.assertEqual(footer, para.parent_story)
self.assertEqual(footer.parent_section, para.parent_section)
self.assertEqual(footer.parent_section, header.parent_section)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.Create.docx')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

