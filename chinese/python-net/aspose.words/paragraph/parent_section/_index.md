---
title: Paragraph.parent_section property
linktitle: parent_section property
articleTitle: parent_section property
second_title: Aspose.Words for Python
description: "Paragraph.parent_section property. Retrieves the parent [Section](../../section/) of the paragraph."
type: docs
weight: 200
url: /zh/python-net/aspose.words/paragraph/parent_section/
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
* class [Paragraph](../)

