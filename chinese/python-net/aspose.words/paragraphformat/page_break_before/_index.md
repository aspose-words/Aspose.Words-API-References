---
title: ParagraphFormat.page_break_before property
linktitle: page_break_before property
articleTitle: page_break_before property
second_title: Aspose.Words for Python
description: "ParagraphFormat.page_break_before property. True if a page break is forced before the paragraph."
type: docs
weight: 270
url: /zh/python-net/aspose.words/paragraphformat/page_break_before/
---

## ParagraphFormat.page_break_before property

True if a page break is forced before the paragraph.


```python
@property
def page_break_before(self) -> bool:
    ...

@page_break_before.setter
def page_break_before(self, value: bool):
    ...

```

### Examples

Shows how to create paragraphs with page breaks at the beginning.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 将此标志设置为 "true" 以在每个段落开头应用分页符
# 文档生成器将在此 ParagraphFormat 配置下创建的内容。
# 第一段将不会出现分页符。
# 将此标志保持为 "false"，以在同一页上开始每个新段落
# 如前所述，前提是有足够的空间。
builder.paragraph_format.page_break_before = page_break_before
builder.writeln('Paragraph 1.')
builder.writeln('Paragraph 2.')
layout_collector = aw.layout.LayoutCollector(doc)
paragraphs = doc.first_section.body.paragraphs
if page_break_before:
    self.assertEqual(1, layout_collector.get_start_page_index(paragraphs[0]))
    self.assertEqual(2, layout_collector.get_start_page_index(paragraphs[1]))
else:
    self.assertEqual(1, layout_collector.get_start_page_index(paragraphs[0]))
    self.assertEqual(1, layout_collector.get_start_page_index(paragraphs[1]))
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.PageBreakBefore.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

