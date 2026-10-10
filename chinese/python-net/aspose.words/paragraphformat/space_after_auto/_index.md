---
title: ParagraphFormat.space_after_auto property
linktitle: space_after_auto property
articleTitle: space_after_auto property
second_title: Aspose.Words for Python
description: "ParagraphFormat.space_after_auto property. True if the amount of spacing after the paragraph is set automatically."
type: docs
weight: 320
url: /zh/python-net/aspose.words/paragraphformat/space_after_auto/
---

## ParagraphFormat.space_after_auto property

True if the amount of spacing after the paragraph is set automatically.


```python
@property
def space_after_auto(self) -> bool:
    ...

@space_after_auto.setter
def space_after_auto(self, value: bool):
    ...

```

### Remarks

When set to ``True``, overrides the effect of [ParagraphFormat.space_after](../space_after/).




When you set paragraph Space Before and Space After to Auto,
Microsoft Word adds 14 points spacing between paragraphs automatically
according to the following rules:


* Normally, spacing is added after all paragraphs.
  
* In a bulleted or numbered list, spacing is added only after the last item in the list.
  Spacing is not added between the list items.
  
* In a nested bulleted or numbered list spacing is not added.
  
* Spacing is normally added after a table.
  
* Spacing is not added after a table if it is the last block in a table cell.
  
* Spacing is not added after the last paragraph in a table cell.
  



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

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

