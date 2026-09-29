---
title: Paragraph.parent_section property
linktitle: parent_section property
articleTitle: parent_section property
second_title: Aspose.Words for Python
description: "Paragraph.parent_section property. Retrieves the parent [Section](../../section/) of the paragraph."
type: docs
weight: 200
url: /sv/python-net/aspose.words/paragraph/parent_section/
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
# Skapa ett sidhuvud och lägg till ett stycke i det. Texten i det stycket
# kommer att visas högst upp på varje sida i detta avsnitt, ovanför huvudtexten.
header = aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_PRIMARY)
doc.first_section.headers_footers.add(header)
para = header.append_paragraph('My header.')
self.assertTrue(header.is_header)
self.assertTrue(para.is_end_of_header_footer)
# Skapa ett sidfot och lägg till ett stycke i det. Texten i det stycket
# kommer att visas längst ner på varje sida i detta avsnitt, under huvudtexten.
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

