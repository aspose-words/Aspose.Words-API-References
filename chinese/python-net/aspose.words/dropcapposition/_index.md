---
title: DropCapPosition enumeration
linktitle: DropCapPosition enumeration
articleTitle: DropCapPosition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.DropCapPosition enumeration. Specifies the position for a drop cap text."
type: docs
weight: 350
url: /zh/python-net/aspose.words/dropcapposition/
---

## DropCapPosition enumeration

Specifies the position for a drop cap text.


### Members

| Name | Description |
| --- | --- |
| NONE | The paragraph does not have a drop cap. |
| NORMAL | The drop cap is positioned inside the text margin on the anchor paragraph. |
| MARGIN | The drop cap is positioned outside the text margin on the anchor paragraph. |

### Examples

Shows how to create a drop cap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入一个段落，其中包含一个大写字母，第二段和第三段的文本以该字母开头。
builder.font.size = 54
builder.writeln('L')
builder.font.size = 18
builder.writeln('orem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ')
builder.writeln('Ut enim ad minim veniam, quis nostrud exercitation ' + 'ullamco laboris nisi ut aliquip ex ea commodo consequat.')
# 目前，第二段和第三段会出现在第一段下面。
# 我们可以通过其“ParagraphFormat”对象将第一段转换为其他段落的首字下沉（drop cap）。
# 将 “DropCapPosition” 属性设置为 “DropCapPosition.Margin” 以将首字下沉放置在
# 页面左侧页边距之外（如果我们的文本是从左到右）。
# 将 “DropCapPosition” 属性设置为 “DropCapPosition.Normal” 以将首字下沉放置在页面边距内
# 并使其余文本环绕它。
# “DropCapPosition.None” 是所有段落的默认状态。
format = doc.first_section.body.first_paragraph.paragraph_format
format.drop_cap_position = drop_cap_position
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.DropCap.docx')
```

### See Also

* module [aspose.words](../)

