---
title: is_end_of_header_footer property
second_title: Aspose.Words for Python via .NET API Reference
description: "True if this paragraph is the last paragraph in the HeaderFooter (main text story) of a Section; false otherwise."
type: docs
weight: 70
url: /python-net/aspose.words/paragraph/is_end_of_header_footer/
---

## Paragraph.is_end_of_header_footer property

True if this paragraph is the last paragraph in the **HeaderFooter** (main text story) of a **Section**; false otherwise.



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
* class [Paragraph](../)

