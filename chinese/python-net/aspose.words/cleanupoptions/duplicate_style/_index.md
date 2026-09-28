---
title: CleanupOptions.duplicate_style property
linktitle: duplicate_style property
articleTitle: duplicate_style property
second_title: Aspose.Words for Python
description: "CleanupOptions.duplicate_style property. Gets/sets a flag indicating whether duplicate styles should be removed from document"
type: docs
weight: 20
url: /zh/python-net/aspose.words/cleanupoptions/duplicate_style/
---

## CleanupOptions.duplicate_style property

Gets/sets a flag indicating whether duplicate styles should be removed from document.
Default value is ``False``.



```python
@property
def duplicate_style(self) -> bool:
    ...

@duplicate_style.setter
def duplicate_style(self, value: bool):
    ...

```

### Examples

Shows how to remove duplicated styles from the document.

```python
doc = aw.Document()
# 向文档添加两个具有相同属性的样式，
# 但名称不同。第二个样式被视为第一个的重复。
my_style = doc.styles.add(aw.StyleType.PARAGRAPH, 'MyStyle1')
my_style.font.size = 14
my_style.font.name = 'Courier New'
my_style.font.color = aspose.pydrawing.Color.blue
duplicate_style = doc.styles.add(aw.StyleType.PARAGRAPH, 'MyStyle2')
duplicate_style.font.size = 14
duplicate_style.font.name = 'Courier New'
duplicate_style.font.color = aspose.pydrawing.Color.blue
self.assertEqual(6, doc.styles.count)
# 将这两种样式应用于文档中不同的段落。
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style_name = my_style.name
builder.writeln('Hello world!')
builder.paragraph_format.style_name = duplicate_style.name
builder.writeln('Hello again!')
paragraphs = doc.first_section.body.paragraphs
self.assertEqual(my_style, paragraphs[0].paragraph_format.style)
self.assertEqual(duplicate_style, paragraphs[1].paragraph_format.style)
# 配置一个 CleanOptions 对象，然后调用 Cleanup 方法来替换所有重复的样式
# 使用原始样式，并从文档中删除重复项。
cleanup_options = aw.CleanupOptions()
cleanup_options.duplicate_style = True
doc.cleanup(cleanup_options)
self.assertEqual(5, doc.styles.count)
self.assertEqual(my_style, paragraphs[0].paragraph_format.style)
self.assertEqual(my_style, paragraphs[1].paragraph_format.style)
```

### See Also

* module [aspose.words](../../)
* class [CleanupOptions](../)

