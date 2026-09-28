---
title: Style.font property
linktitle: font property
articleTitle: font property
second_title: Aspose.Words for Python
description: "Style.font property. Gets the character formatting of the style."
type: docs
weight: 60
url: /zh/python-net/aspose.words/style/font/
---

## Style.font property

Gets the character formatting of the style.


```python
@property
def font(self) -> aspose.words.Font:
    ...

```

### Remarks

For list styles this property returns ``None``.




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

Shows how to create and use a paragraph style with list formatting.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 创建自定义段落样式。
style = doc.styles.add(aw.StyleType.PARAGRAPH, 'MyStyle1')
style.font.size = 24
style.font.name = 'Verdana'
style.paragraph_format.space_after = 12
# 创建列表并确保使用此样式的段落将使用该列表。
style.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
style.list_format.list_level_number = 0
# 将段落样式应用于文档构建器的当前段落，然后添加一些文本。
builder.paragraph_format.style = style
builder.writeln('Hello World: MyStyle1, bulleted list.')
# 将文档构建器的样式更改为没有列表格式的样式，并写入另一段落。
builder.paragraph_format.style = doc.styles.get_by_name('Normal')
builder.writeln('Hello World: Normal.')
builder.document.save(file_name=ARTIFACTS_DIR + 'Styles.ParagraphStyleBulletedList.docx')
```

### See Also

* module [aspose.words](../../)
* class [Style](../)

