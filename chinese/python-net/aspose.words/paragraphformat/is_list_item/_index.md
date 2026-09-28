---
title: ParagraphFormat.is_list_item property
linktitle: is_list_item property
articleTitle: is_list_item property
second_title: Aspose.Words for Python
description: "ParagraphFormat.is_list_item property. True when the paragraph is an item in a bulleted or numbered list."
type: docs
weight: 150
url: /zh/python-net/aspose.words/paragraphformat/is_list_item/
---

## ParagraphFormat.is_list_item property

True when the paragraph is an item in a bulleted or numbered list.


```python
@property
def is_list_item(self) -> bool:
    ...

```

### Examples

Shows how to nest a list inside another list.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
# 我们可以通过增加缩进级别来创建嵌套列表。
# 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
# 我们在列表的开始和结束之间添加的每个段落都会成为列表中的一项。
# 为标题创建大纲列表。
outline_list = doc.lists.add(list_template=aw.lists.ListTemplate.OUTLINE_NUMBERS)
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('This is my Chapter 1')
# 创建编号列表。
numbered_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
builder.list_format.list = numbered_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.writeln('Numbered list item 1.')
# 每个组成列表的段落都会具有此标志。
self.assertTrue(builder.current_paragraph.is_list_item)
self.assertTrue(builder.paragraph_format.is_list_item)
# 创建项目符号列表。
bulleted_list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
builder.list_format.list = bulleted_list
builder.paragraph_format.left_indent = 72
builder.writeln('Bulleted list item 1.')
builder.writeln('Bulleted list item 2.')
builder.paragraph_format.clear_formatting()
# 恢复为编号列表。
builder.list_format.list = numbered_list
builder.writeln('Numbered list item 2.')
builder.writeln('Numbered list item 3.')
# 恢复为大纲列表。
builder.list_format.list = outline_list
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('This is my Chapter 2')
builder.paragraph_format.clear_formatting()
builder.document.save(file_name=ARTIFACTS_DIR + 'Lists.NestedLists.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

