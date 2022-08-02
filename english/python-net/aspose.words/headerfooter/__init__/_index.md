---
title: HeaderFooter constructor
second_title: Aspose.Words for Python via .NET API Reference
description: "Creates a new header or footer of the specified type."
type: docs
weight: 10
url: /python-net/aspose.words/headerfooter/__init__/
---

## HeaderFooter(doc, header_footer_type) {#documentbase_headerfootertype}

Creates a new header or footer of the specified type.


```python
def __init__(self, doc: aspose.words.DocumentBase, header_footer_type: aspose.words.HeaderFooterType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) |  |
| header_footer_type | [HeaderFooterType](../../headerfootertype/) |  |

When **HeaderFooter** is created, it belongs to the specified document, but is not
yet part of the document and **ParentNode** is null.

To append **HeaderFooter** to a **Section** use Section.InsertAfter, Section.InsertBefore,
HeadersFooters.Add or HeadersFooters.Insert.




### Examples

Shows how to create a header and a footer.

```python
doc = aw.Document()

# Create a header and append a paragraph to it. The text in that paragraph
# will appear at the top of every page of this section, above the main body text.
header = aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_PRIMARY)
doc.first_section.headers_footers.add(header)

para = header.append_paragraph("My header.")

self.assertTrue(header.is_header)
self.assertTrue(para.is_end_of_header_footer)

# Create a footer and append a paragraph to it. The text in that paragraph
# will appear at the bottom of every page of this section, below the main body text.
footer = aw.HeaderFooter(doc, aw.HeaderFooterType.FOOTER_PRIMARY)
doc.first_section.headers_footers.add(footer)

para = footer.append_paragraph("My footer.")

self.assertFalse(footer.is_header)
self.assertTrue(para.is_end_of_header_footer)

self.assertEqual(footer, para.parent_story)
self.assertEqual(footer.parent_section, para.parent_section)
self.assertEqual(footer.parent_section, header.parent_section)

doc.save(ARTIFACTS_DIR + "HeaderFooter.create.docx")
```

### See Also

* module [aspose.words](../../)
* class [HeaderFooter](../)

