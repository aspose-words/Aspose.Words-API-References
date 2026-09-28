---
title: ParagraphFormat.widow_control property
linktitle: widow_control property
articleTitle: widow_control property
second_title: Aspose.Words for Python
description: "ParagraphFormat.widow_control property. True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph."
type: docs
weight: 410
url: /zh/python-net/aspose.words/paragraphformat/widow_control/
---

## ParagraphFormat.widow_control property

True if the first and last lines in the paragraph are to remain on the same page as the rest of the paragraph.


```python
@property
def widow_control(self) -> bool:
    ...

@widow_control.setter
def widow_control(self, value: bool):
    ...

```

### Examples

Shows how to enable widow/orphan control for a paragraph.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 当我们编写的文本无法容纳在一页时，可能会有一行溢出到下一页。
# 最终出现在下一页的单行称为 "Orphan"（孤行），
# 而导致孤行断开的前一行称为 "Widow"（寡行）。
# 我们可以通过调整字体大小、间距或页面边距来修复孤行和寡行。
# 如果我们希望保持文档的尺寸，可以将此标志设置为 "true"
# 以将寡行推到与其对应的孤行同一页。
# 将此标志保持为 "false" 将在文本中保留寡行/孤行对。
# 每个段落都有此设置，可在 Microsoft Word 中通过 “主页 -> 段落 -> 段落设置” 访问
# （位于 "Paragraph" 选项卡右下角的按钮）-> "Widow/Orphan control”。
builder.paragraph_format.widow_control = widow_control
# 插入会产生孤行和寡行的文本。
builder.font.size = 68
builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.WidowControl.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

