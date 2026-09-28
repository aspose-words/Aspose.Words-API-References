---
title: DocumentBase.styles property
linktitle: styles property
articleTitle: styles property
second_title: Aspose.Words for Python
description: "DocumentBase.styles property. Returns a collection of styles defined in the document."
type: docs
weight: 90
url: /zh/python-net/aspose.words/documentbase/styles/
---

## DocumentBase.styles property

Returns a collection of styles defined in the document.


```python
@property
def styles(self) -> aspose.words.StyleCollection:
    ...

```

### Remarks

For more information see the description of the [StyleCollection](../../stylecollection/) class.




### Examples

Shows how to access a document's style collection.

```python
doc = aw.Document()
self.assertEqual(4, doc.styles.count)
# 枚举并列出使用 Aspose.Words 创建的文档默认包含的所有样式。
for cur_style in doc.styles:
    print(f'Style name:\t"{cur_style.name}", of type "{cur_style.type}"')
    print(f'\tSubsequent style:\t{cur_style.next_paragraph_style_name}')
    print(f'\tIs heading:\t\t\t{cur_style.is_heading}')
    print(f'\tIs QuickStyle:\t\t{cur_style.is_quick_style}')
    self.assertEqual(doc, cur_style.document)
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
* class [DocumentBase](../)
* class [StyleCollection](../../stylecollection/)
* class [Style](../../style/)

