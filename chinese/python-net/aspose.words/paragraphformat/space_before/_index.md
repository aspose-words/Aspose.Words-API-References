---
title: ParagraphFormat.space_before property
linktitle: space_before property
articleTitle: space_before property
second_title: Aspose.Words for Python
description: "ParagraphFormat.space_before property. Gets or sets the amount of spacing (in points) before the paragraph."
type: docs
weight: 330
url: /zh/python-net/aspose.words/paragraphformat/space_before/
---

## ParagraphFormat.space_before property

Gets or sets the amount of spacing (in points) before the paragraph.


```python
@property
def space_before(self) -> float:
    ...

@space_before.setter
def space_before(self, value: float):
    ...

```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | Throws when argument was out of the range of valid values. |

### Remarks

Has no effect when [ParagraphFormat.space_before_auto](../space_before_auto/) is ``True``.

Valid values range from 0 to 1584 inclusive.




### Examples

Shows how to set automatic paragraph spacing.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 对该构建器将创建的段落前后应用大量间距。
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24
# 将这些标志设置为 "true" 以应用自动间距，
# 实际上会忽略我们在上面设置的属性间距。
# 将它们保持为 "false" 将使用我们自定义的段落间距。
builder.paragraph_format.space_after_auto = auto_spacing
builder.paragraph_format.space_before_auto = auto_spacing
# 插入两个段落，使其上下都有间距，然后保存文档。
builder.writeln('Paragraph 1.')
builder.writeln('Paragraph 2.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphSpacingAuto.docx')
```

Shows how to apply no spacing between paragraphs with the same style.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 对该构建器将创建的段落前后应用大量间距。
builder.paragraph_format.space_before = 24
builder.paragraph_format.space_after = 24
# 将 “NoSpaceBetweenParagraphsOfSameStyle” 标志设置为 “true” 以应用
# 相同样式段落之间不留间距，这将把相似段落归为一组。
# 将 “NoSpaceBetweenParagraphsOfSameStyle” 标志保持为 “false”
# 以均匀地对每个段落应用间距。
builder.paragraph_format.no_space_between_paragraphs_of_same_style = no_space_between_paragraphs_of_same_style
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.paragraph_format.style = doc.styles.get_by_name('Quote')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
builder.writeln(f'Paragraph in the "{builder.paragraph_format.style.name}" style.')
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.ParagraphSpacingSameStyle.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

