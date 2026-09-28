---
title: Style.automatically_update property
linktitle: automatically_update property
articleTitle: automatically_update property
second_title: Aspose.Words for Python
description: "Style.automatically_update property. Specifies whether this style is automatically redefined based on the appropriate value."
type: docs
weight: 20
url: /zh/python-net/aspose.words/style/automatically_update/
---

## Style.automatically_update property

Specifies whether this style is automatically redefined based on the appropriate value.


```python
@property
def automatically_update(self) -> bool:
    ...

@automatically_update.setter
def automatically_update(self, value: bool):
    ...

```

### Remarks

If the property value is set to true, MS Word automatically redefines the current style when
the appropriate paragraph formatting has been changed.

AutomaticallyUpdate property is applicable to paragraph styles only.

The default value is ``False``.




### Examples

Shows how to create and apply a custom style.

```python
doc = aw.Document()
style = doc.styles.add(aw.StyleType.PARAGRAPH, 'MyStyle')
style.font.name = 'Times New Roman'
style.font.size = 16
style.font.color = aspose.pydrawing.Color.navy
# 自动重新定义样式。
style.automatically_update = True
builder = aw.DocumentBuilder(doc=doc)
# 将文档中的一种样式应用于文档构建器正在创建的段落。
builder.paragraph_format.style = doc.styles.get_by_name('MyStyle')
builder.writeln('Hello world!')
first_paragraph_style = doc.first_section.body.first_paragraph.paragraph_format.style
self.assertEqual(style, first_paragraph_style)
# 从文档的样式集合中移除我们的自定义样式。
doc.styles.get_by_name('MyStyle').remove()
first_paragraph_style = doc.first_section.body.first_paragraph.paragraph_format.style
# 任何使用了已移除样式的文本将恢复为默认格式。
self.assertFalse(any([s.name == 'MyStyle' for s in doc.styles]))
self.assertEqual('Times New Roman', first_paragraph_style.font.name)
self.assertEqual(12, first_paragraph_style.font.size)
self.assertEqual(aspose.pydrawing.Color.empty().to_argb(), first_paragraph_style.font.color.to_argb())
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

