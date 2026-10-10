---
title: ParagraphFormat.lines_to_drop property
linktitle: lines_to_drop property
articleTitle: lines_to_drop property
second_title: Aspose.Words for Python
description: "ParagraphFormat.lines_to_drop property. Gets or sets the number of lines of the paragraph text used to calculate the drop cap height."
type: docs
weight: 230
url: /zh/python-net/aspose.words/paragraphformat/lines_to_drop/
---

## ParagraphFormat.lines_to_drop property

Gets or sets the number of lines of the paragraph text used to calculate the drop cap height.


```python
@property
def lines_to_drop(self) -> int:
    ...

@lines_to_drop.setter
def lines_to_drop(self, value: int):
    ...

```

### Examples

Shows how to set the size of a drop cap.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 修改 “LinesToDrop” 属性以将段落指定为首字下沉（drop cap），
# 这将把它转换为一个大写字母，用于装饰下一段。
# 将此属性的值设为 4，以使首字母的高度为四行文本。
builder.paragraph_format.lines_to_drop = 4
builder.writeln('H')
# 将 "LinesToDrop" 属性重置为 0，以将下一段转换为普通段落。
# 此段落中的文本将环绕首字母。
builder.paragraph_format.lines_to_drop = 0
builder.writeln('ello world!')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.LinesToDrop.odt')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

