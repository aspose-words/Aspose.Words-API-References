---
title: ListFormat.is_list_item property
linktitle: is_list_item property
articleTitle: is_list_item property
second_title: Aspose.Words for Python
description: "ListFormat.is_list_item property. True when the paragraph has bulleted or numbered formatting applied to it."
type: docs
weight: 10
url: /zh/python-net/aspose.words.lists/listformat/is_list_item/
---

## ListFormat.is_list_item property

True when the paragraph has bulleted or numbered formatting applied to it.


```python
@property
def is_list_item(self) -> bool:
    ...

```

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

Shows how to output all paragraphs in a document that are list items.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.list_format.apply_number_default()
builder.writeln('Numbered list item 1')
builder.writeln('Numbered list item 2')
builder.writeln('Numbered list item 3')
builder.list_format.remove_numbers()
builder.list_format.apply_bullet_default()
builder.writeln('Bulleted list item 1')
builder.writeln('Bulleted list item 2')
builder.writeln('Bulleted list item 3')
builder.list_format.remove_numbers()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
for para in list(filter(lambda p: p.list_format.is_list_item, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras)))))):
    print(f'This paragraph belongs to list ID# {para.list_format.list.list_id}, number style "{para.list_format.list_level.number_style}"')
    print(f'\t"{para.get_text().strip()}"')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListFormat](../)

