---
title: Paragraph.is_end_of_header_footer property
linktitle: is_end_of_header_footer property
articleTitle: is_end_of_header_footer property
second_title: Aspose.Words for Python
description: "Paragraph.is_end_of_header_footer property. True if this paragraph is the last paragraph in the [HeaderFooter](../../headerfooter/) (main text story) of a [Section](../../section/); false otherwise."
type: docs
weight: 70
url: /es/python-net/aspose.words/paragraph/is_end_of_header_footer/
---

## Paragraph.is_end_of_header_footer property

True if this paragraph is the last paragraph in the [HeaderFooter](../../headerfooter/) (main text story) of a [Section](../../section/); false otherwise.



```python
@property
def is_end_of_header_footer(self) -> bool:
    ...

```

### Examples

Shows how to create a header and a footer.

```python
doc = aw.Document()
# Cree un encabezado y añada un párrafo a él. El texto en ese párrafo
# aparecerá en la parte superior de cada página de esta sección, sobre el texto principal.
header = aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_PRIMARY)
doc.first_section.headers_footers.add(header)
para = header.append_paragraph('My header.')
self.assertTrue(header.is_header)
self.assertTrue(para.is_end_of_header_footer)
# Cree un pie de página y añada un párrafo a él. El texto en ese párrafo
# aparecerá en la parte inferior de cada página de esta sección, bajo el texto principal.
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

