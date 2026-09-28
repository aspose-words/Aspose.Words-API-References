---
title: ListCollection class
linktitle: ListCollection class
articleTitle: ListCollection class
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListCollection class. Stores and manages formatting of bulleted and numbered lists used in a document"
type: docs
weight: 20
url: /zh/python-net/aspose.words.lists/listcollection/
---

## ListCollection class

Stores and manages formatting of bulleted and numbered lists used in a document.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/python-net/working-with-lists/) documentation article.




### Remarks

A list in a Microsoft Word document is a set of list formatting properties.
The formatting of the lists is stored in the [ListCollection](./) collection separately
from the paragraphs of text.

You do not create objects of this class. There is always only one [ListCollection](./)
object per document and it is accessible via the [DocumentBase.lists](../../aspose.words/documentbase/lists/) property.

To create a new list based on a predefined list template or based on a list style,
use the [ListCollection.add()](./add/#style) method.

To create a new list with formatting identical to an existing list,
use the [ListCollection.add_copy()](./add_copy/#list) method.

To make a paragraph bulleted or numbered, you need to apply list formatting
to a paragraph by assigning a [List](../list/) object to the
[ListFormat.list](../listformat/list/) property of [ListFormat](../listformat/).

To remove list formatting from a paragraph, use the [ListFormat.remove_numbers()](../listformat/remove_numbers/#default)
method.

If you know a bit about WordprocessingML, then you might know it defines separate concepts
for "list" and "list definition". This exactly corresponds to how list formatting is stored
in a Microsoft Word document at the low level. List definition is like a "schema" and
list is like an instance of a list definition.

To simplify programming model, Aspose.Words hides the distinction between list and list
definition in much the same way like Microsoft Word hides this in its user interface.
This allows you to concentrate more on how you want your document to look like, rather than
building low-level objects to satisfy requirements of the Microsoft Word file format.

It is not possible to delete lists once they are created in the current version of Aspose.Words.
This is similar to Microsoft Word where user does not have explicit control over list definitions.




### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) | Gets a list by index. |

### Properties

| Name | Description |
| --- | --- |
| [count](./count/) | Gets the count of numbered and bulleted lists in the document. |
| [document](./document/) | Gets the owner document. |

### Methods

| Name | Description |
| --- | --- |
|[ add(list_template)](./add/#listtemplate) | Creates a new list based on a predefined template and adds it to the collection of lists in the document. |
|[ add(list_style)](./add/#style) | Creates a new list that references a list style and adds it to the collection of lists in the document. |
|[ add_copy(src_list)](./add_copy/#list) | Creates a new list by copying the specified list and adding it to the collection of lists in the document. |
|[ add_single_level_list(list_template)](./add_single_level_list/#listtemplate) | Creates a new single level list based on the predefined template and adds it to the list collection in the document. |
|[ get_list_by_list_id(list_id)](./get_list_by_list_id/#int) | Gets a list by a list identifier. |

### Examples

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

Shows how to restart numbering in a list by copying a list.

```python
doc = aw.Document()
# 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
# 我们可以通过增加缩进级别来创建嵌套列表。
# 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
# 我们在列表的开始和结束之间添加的每个段落都会成为列表中的一项。
# 从 Microsoft Word 模板创建列表，并自定义其第一级列表。
list1 = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_ARABIC_PARENTHESIS)
list1.list_levels[0].font.color = aspose.pydrawing.Color.red
list1.list_levels[0].alignment = aw.lists.ListLevelAlignment.RIGHT
# 将我们的列表应用于一些段落。
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('List 1 starts below:')
builder.list_format.list = list1
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
# 我们可以将现有列表的副本添加到文档的列表集合中
# 以创建相似的列表而不更改原始列表。
list2 = doc.lists.add_copy(list1)
list2.list_levels[0].font.color = aspose.pydrawing.Color.blue
list2.list_levels[0].start_at = 10
# 将第二个列表应用于新段落。
builder.writeln('List 2 starts below:')
builder.list_format.list = list2
builder.writeln('Item 1')
builder.writeln('Item 2')
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.RestartNumberingUsingListCopy.docx')
```

Shows how to create a document with a sample of all the lists from another document.

```python
src_doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
dst_doc = aw.Document()
builder = aw.DocumentBuilder(doc=dst_doc)
for src_list in src_doc.lists:
    dst_list = dst_doc.lists.add_copy(src_list)
    ExLists._add_list_sample(builder, dst_list)
dst_doc.save(file_name=ARTIFACTS_DIR + 'Lists.PrintOutAllLists.docx')
```

Shows how to create a document with a sample of all the lists from another document (AddListSample).

```python
@staticmethod
def _add_list_sample(builder, doc_list):
    builder.writeln('Sample formatting of list with ListId:' + str(doc_list.list_id))
    builder.list_format.list = doc_list
    i = 0
    while i < doc_list.list_levels.count:
        builder.list_format.list_level_number = i
        builder.writeln('Level ' + str(i))
        i += 1
    builder.list_format.remove_numbers()
    builder.writeln()
```

### See Also

* module [aspose.words.lists](../)
* class [List](../list/)
* class [ListLevel](../listlevel/)
* class [ListFormat](../listformat/)

