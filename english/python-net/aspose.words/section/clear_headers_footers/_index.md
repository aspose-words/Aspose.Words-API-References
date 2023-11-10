---
title: Section.clear_headers_footers method
linktitle: clear_headers_footers method
articleTitle: clear_headers_footers method
second_title: Aspose.Words for Python
description: "Section.clear_headers_footers method. Clears the headers and footers of this section."
type: docs
weight: 100
url: /python-net/aspose.words/section/clear_headers_footers/
---

## clear_headers_footers() {#default}

Clears the headers and footers of this section.


```python
def clear_headers_footers(self):
    ...
```

### Remarks

The text of all headers and footers is cleared, but [HeaderFooter](../../headerfooter/) objects themselves are not removed.

This makes headers and footers of this section linked to headers and footers of the previous section.




### Examples

Shows how to clear the contents of all headers and footers in a section.

```python
doc = aw.Document()

self.assertEqual(0, doc.first_section.headers_footers.count)

builder = aw.DocumentBuilder(doc)

builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.writeln("This is the primary header.")
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.writeln("This is the primary footer.")

self.assertEqual(2, doc.first_section.headers_footers.count)

self.assertEqual("This is the primary header.", doc.first_section.headers_footers.header_primary.get_text().strip())
self.assertEqual("This is the primary footer.", doc.first_section.headers_footers.footer_primary.get_text().strip())

# Empty all the headers and footers in this section of all their contents.
# The headers and footers themselves will still be present but will have nothing to display.
doc.first_section.clear_headers_footers()

self.assertEqual(2, doc.first_section.headers_footers.count)

self.assertEqual("", doc.first_section.headers_footers.header_primary.get_text().strip())
self.assertEqual("", doc.first_section.headers_footers.footer_primary.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

