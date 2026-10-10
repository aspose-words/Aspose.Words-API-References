---
title: HeaderFooter.header_footer_type property
linktitle: header_footer_type property
articleTitle: header_footer_type property
second_title: Aspose.Words for Python
description: "HeaderFooter.header_footer_type property. Gets the type of this header/footer."
type: docs
weight: 20
url: /it/python-net/aspose.words/headerfooter/header_footer_type/
---

## HeaderFooter.header_footer_type property

Gets the type of this header/footer.


```python
@property
def header_footer_type(self) -> aspose.words.HeaderFooterType:
    ...

```

### Examples

Shows how to create a header and a footer.

```python
doc = aw.Document()
# Crea un'intestazione e aggiungi un paragrafo ad essa. Il testo in quel paragrafo
# apparirà nella parte superiore di ogni pagina di questa sezione, sopra il testo principale.
header = aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_PRIMARY)
doc.first_section.headers_footers.add(header)
para = header.append_paragraph('My header.')
self.assertTrue(header.is_header)
self.assertTrue(para.is_end_of_header_footer)
# Crea un piè di pagina e aggiungi un paragrafo ad esso. Il testo in quel paragrafo
# apparirà nella parte inferiore di ogni pagina di questa sezione, sotto il testo principale.
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

