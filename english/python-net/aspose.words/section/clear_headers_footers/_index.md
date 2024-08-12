---
title: Section.clear_headers_footers method
linktitle: clear_headers_footers method
articleTitle: clear_headers_footers method
second_title: Aspose.Words for Python
description: "aspose.words.Section.clear_headers_footers method"
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




## clear_headers_footers(preserve_watermarks) {#bool}

Clears the headers and footers of this section.


```python
def clear_headers_footers(self, preserve_watermarks: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| preserve_watermarks | bool | True if the watermarks shall not be removed. |

### Remarks

The text of all headers and footers is cleared, but [HeaderFooter](../../headerfooter/) objects themselves are not removed.

This makes headers and footers of this section linked to headers and footers of the previous section.




## Examples

Shows how to clear the contents of header and footer with or without a watermark.

```python
doc = aw.Document(file_name=MY_DIR + 'Header and footer types.docx')
# Add a plain text watermark.
doc.watermark.set_text(text='Aspose Watermark')
# Make sure the headers and footers have content.
headers_footers = doc.first_section.headers_footers
self.assertEqual('First header', headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_FIRST).get_text().strip())
self.assertEqual('Second header', headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_EVEN).get_text().strip())
self.assertEqual('Third header', headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_PRIMARY).get_text().strip())
self.assertEqual('First footer', headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_FIRST).get_text().strip())
self.assertEqual('Second footer', headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_EVEN).get_text().strip())
self.assertEqual('Third footer', headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY).get_text().strip())
# Removes all header and footer content except watermarks.
doc.first_section.clear_headers_footers(True)
headers_footers = doc.first_section.headers_footers
self.assertEqual('', headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_FIRST).get_text().strip())
self.assertEqual('', headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_EVEN).get_text().strip())
self.assertEqual('', headers_footers.get_by_header_footer_type(aw.HeaderFooterType.HEADER_PRIMARY).get_text().strip())
self.assertEqual('', headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_FIRST).get_text().strip())
self.assertEqual('', headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_EVEN).get_text().strip())
self.assertEqual('', headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY).get_text().strip())
self.assertEqual(aw.WatermarkType.TEXT, doc.watermark.type)
# Removes all header and footer content including watermarks.
doc.first_section.clear_headers_footers(False)
self.assertEqual(aw.WatermarkType.NONE, doc.watermark.type)
```

## See Also

* module [aspose.words](../../)
* class [Section](../)

