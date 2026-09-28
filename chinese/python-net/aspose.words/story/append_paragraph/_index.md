---
title: Story.append_paragraph method
linktitle: append_paragraph method
articleTitle: append_paragraph method
second_title: Aspose.Words for Python
description: "Story.append_paragraph method. A shortcut method that creates a [Paragraph](../../paragraph/) object with optional text and appends it to the end of this object."
type: docs
weight: 60
url: /zh/python-net/aspose.words/story/append_paragraph/
---

## append_paragraph(text) {#str}

A shortcut method that creates a [Paragraph](../../paragraph/) object with optional text and appends it to the end of this object.



```python
def append_paragraph(self, text: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| text | str | The text for the paragraph. Can be ``None`` or empty string. |

### Returns

The newly created and appended paragraph.


### Examples

Shows how to create a header and a footer.

```python
doc = aw.Document()
# 创建页眉并向其追加一个段落。该段落中的文本
# 将出现在本节每页的顶部，主正文文本之上。
header = aw.HeaderFooter(doc, aw.HeaderFooterType.HEADER_PRIMARY)
doc.first_section.headers_footers.add(header)
para = header.append_paragraph('My header.')
self.assertTrue(header.is_header)
self.assertTrue(para.is_end_of_header_footer)
# 创建页脚并向其追加一个段落。该段落中的文本
# 将出现在本节每页的底部，主正文文本之下。
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
* class [Story](../)

