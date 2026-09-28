---
title: ListLevel.number_position property
linktitle: number_position property
articleTitle: number_position property
second_title: Aspose.Words for Python
description: "ListLevel.number_position property. Returns or sets the position (in points) of the number or bullet for the list level."
type: docs
weight: 80
url: /zh/python-net/aspose.words.lists/listlevel/number_position/
---

## ListLevel.number_position property

Returns or sets the position (in points) of the number or bullet for the list level.


```python
@property
def number_position(self) -> float:
    ...

@number_position.setter
def number_position(self, value: float):
    ...

```

### Remarks

[ListLevel.number_position](./) corresponds to LeftIndent plus FirstLineIndent of the paragraph.




### Examples

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```python
doc = aw.Document()
# 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
# 我们可以通过增加缩进级别来创建嵌套列表。
# 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
# 我们在列表的开始和结束之间添加的每个段落都会成为列表中的一项。
# 从 Microsoft Word 模板创建列表，并自定义其前两个列表级别。
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
list_level = doc_list.list_levels[0]
list_level.font.color = aspose.pydrawing.Color.red
list_level.font.size = 24
list_level.number_style = aw.NumberStyle.ORDINAL_TEXT
list_level.start_at = 21
list_level.number_format = '\x00'
list_level.number_position = -36
list_level.text_position = 144
list_level.tab_position = 144
list_level = doc_list.list_levels[1]
list_level.alignment = aw.lists.ListLevelAlignment.RIGHT
list_level.number_style = aw.NumberStyle.BULLET
list_level.font.name = 'Wingdings'
list_level.font.color = aspose.pydrawing.Color.blue
list_level.font.size = 24
# 此 NumberFormat 值将创建星形项目符号列表符号。
list_level.number_format = '\uf0af'
list_level.trailing_character = aw.lists.ListTrailingCharacter.SPACE
list_level.number_position = 144
# 创建段落并将我们自定义列表格式的两个列表级别应用于它们。
builder = aw.DocumentBuilder(doc=doc)
builder.list_format.list = doc_list
builder.writeln('The quick brown fox...')
builder.writeln('The quick brown fox...')
builder.list_format.list_indent()
builder.writeln('jumped over the lazy dog.')
builder.writeln('jumped over the lazy dog.')
builder.list_format.list_outdent()
builder.writeln('The quick brown fox...')
builder.list_format.remove_numbers()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.CreateCustomList.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)
* property [ListLevel.text_position](../text_position/)
* property [ListLevel.tab_position](../tab_position/)

