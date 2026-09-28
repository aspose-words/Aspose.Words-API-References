---
title: ListFormat.list_level_number property
linktitle: list_level_number property
articleTitle: list_level_number property
second_title: Aspose.Words for Python
description: "ListFormat.list_level_number property. Gets or sets the list level number (0 to 8) for the paragraph."
type: docs
weight: 40
url: /zh/python-net/aspose.words.lists/listformat/list_level_number/
---

## ListFormat.list_level_number property

Gets or sets the list level number (0 to 8) for the paragraph.


```python
@property
def list_level_number(self) -> int:
    ...

@list_level_number.setter
def list_level_number(self, value: int):
    ...

```

### Remarks

In Word documents, lists may consist of 1 or 9 levels, numbered 0 to 8.

Has effect only when the [ListFormat.list](../list/) property is set to reference a valid list.




### Examples

Shows how to create bulleted and numbered lists.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Aspose.Words main advantages are:')
# 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
# 我们可以通过增加缩进级别来创建嵌套列表。
# 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
# 我们在列表的开始和结束之间添加的每个段落都会成为列表中的一项。
# 以下是我们可以使用文档生成器创建的两种列表类型。
# 1 -  项目符号列表：
# 此列表将在每个段落前应用缩进和项目符号 ("•")。
builder.list_format.apply_bullet_default()
builder.writeln('Great performance')
builder.writeln('High reliability')
builder.writeln('Quality code and working')
builder.writeln('Wide variety of features')
builder.writeln('Easy to understand API')
# 结束项目符号列表。
builder.list_format.remove_numbers()
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
builder.writeln('Aspose.Words allows:')
# 2 -  编号列表：
# 编号列表通过为每个项目编号，为段落创建逻辑顺序。
builder.list_format.apply_number_default()
# 此段落是第一项。编号列表的第一项将使用 "1." 作为其列表项符号。
builder.writeln('Opening documents from different formats:')
self.assertEqual(0, builder.list_format.list_level_number)
# 调用 "ListIndent" 方法以增加当前列表级别，
# 这将在第一级列表的当前项处启动一个新的独立列表，具有更深的缩进。
builder.list_format.list_indent()
self.assertEqual(1, builder.list_format.list_level_number)
# 以下是第二级列表的前三个列表项，它们将保持计数
# 独立于第一级列表的计数。根据当前列表格式，
# 它们将使用 "a.", "b.", 和 "c." 作为符号。
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
# 调用 "ListOutdent" 方法返回到上一级列表。
builder.list_format.list_outdent()
self.assertEqual(0, builder.list_format.list_level_number)
# 这两个段落将继续第一级列表的计数。
# 这些项将使用 "2.", 和 "3." 作为符号
builder.writeln('Processing documents')
builder.writeln('Saving documents in different formats:')
# 如果我们将列表级别提升到之前已添加项目的级别，
# 嵌套列表将与之前的列表分离，并且其编号将从头开始。
# 这些列表项将使用符号 "a.", "b.", "c.", "d.", 和 "e"。
builder.list_format.list_indent()
builder.writeln('DOC')
builder.writeln('PDF')
builder.writeln('HTML')
builder.writeln('MHTML')
builder.writeln('Plain text')
# 再次将列表级别向左缩进。
builder.list_format.list_outdent()
builder.writeln('Doing many other things!')
# 结束编号列表。
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.ApplyDefaultBulletsAndNumbers.docx')
```

Shows how to work with list levels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
self.assertFalse(builder.list_format.is_list_item)
# 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
# 我们可以通过增加缩进级别来创建嵌套列表。
# 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
# 我们在列表的开始和结束之间添加的每个段落都会成为列表中的一项。
# 下面是使用文档生成器可以创建的两种列表类型。
# 1 -  编号列表：
# 编号列表通过为每个项目编号，为段落创建逻辑顺序。
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
self.assertTrue(builder.list_format.is_list_item)
# 通过设置 "ListLevelNumber" 属性，我们可以提升列表级别
# 以在当前列表项处开始一个独立的子列表。
# 名为 "NumberDefault" 的 Microsoft Word 列表模板使用数字来创建第一列表级别的列表层级。
# 更深的列表级别使用字母和小写罗马数字。
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 2 -  项目符号列表：
# 此列表将在每个段落前应用缩进和项目符号 ("•")。
# 此列表的更深层级将使用不同的符号，例如 "■" 和 "○"。
builder.list_format.list = doc.lists.add(list_template=aw.lists.ListTemplate.BULLET_DEFAULT)
i = 0
while i < 9:
    builder.list_format.list_level_number = i
    builder.writeln('Level ' + str(i))
    i += 1
# 我们可以通过取消设置 "List" 标志来禁用列表格式，从而不将后续段落格式化为列表。
builder.list_format.list = None
self.assertFalse(builder.list_format.is_list_item)
doc.save(file_name=ARTIFACTS_DIR + 'Lists.SpecifyListLevel.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)
* property [ListFormat.list](../list/)

