---
title: HeaderFooter.is_header property
linktitle: is_header property
articleTitle: is_header property
second_title: Aspose.Words for Python
description: "HeaderFooter.is_header property. True if this [HeaderFooter](../) object is a header."
type: docs
weight: 30
url: /es/python-net/aspose.words/headerfooter/is_header/
---

## HeaderFooter.is_header property

True if this [HeaderFooter](../) object is a header.



```python
@property
def is_header(self) -> bool:
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
* class [HeaderFooter](../)

