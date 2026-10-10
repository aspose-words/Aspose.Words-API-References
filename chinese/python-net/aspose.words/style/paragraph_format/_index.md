---
title: Style.paragraph_format property
linktitle: paragraph_format property
articleTitle: paragraph_format property
second_title: Aspose.Words for Python
description: "Style.paragraph_format property. Gets the paragraph formatting of the style."
type: docs
weight: 150
url: /zh/python-net/aspose.words/style/paragraph_format/
---

## Style.paragraph_format property

Gets the paragraph formatting of the style.


```python
@property
def paragraph_format(self) -> aspose.words.ParagraphFormat:
    ...

```

### Remarks

For character and list styles this property returns ``None``.




### Examples

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

