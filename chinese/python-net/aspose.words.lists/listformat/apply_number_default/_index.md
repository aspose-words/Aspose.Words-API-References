---
title: ListFormat.apply_number_default method
linktitle: apply_number_default method
articleTitle: apply_number_default method
second_title: Aspose.Words for Python
description: "ListFormat.apply_number_default method. Starts a new default numbered list and applies it to the paragraph."
type: docs
weight: 60
url: /zh/python-net/aspose.words.lists/listformat/apply_number_default/
---

## apply_number_default() {#default}

Starts a new default numbered list and applies it to the paragraph.


```python
def apply_number_default(self):
    ...
```

### Remarks

This is a shortcut method that creates a new list using the default numbered
template, applies it to the paragraph and selects the 1st list level.




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

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)
* property [ListFormat.list](../list/)
* method [ListFormat.remove_numbers()](../remove_numbers/#default)
* property [ListFormat.list_level_number](../list_level_number/)

