---
title: ListLevel.is_legal property
linktitle: is_legal property
articleTitle: is_legal property
second_title: Aspose.Words for Python
description: "ListLevel.is_legal property. True if the level turns all inherited numbers to Arabic, false if it preserves their number style."
type: docs
weight: 50
url: /zh/python-net/aspose.words.lists/listlevel/is_legal/
---

## ListLevel.is_legal property

True if the level turns all inherited numbers to Arabic, false if it preserves their number style.


```python
@property
def is_legal(self) -> bool:
    ...

@is_legal.setter
def is_legal(self, value: bool):
    ...

```

### Examples

Shows advances ways of customizing list labels.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 列表允许我们使用前缀符号和缩进来组织和装饰段落集合。
# 我们可以通过增加缩进级别来创建嵌套列表。
# 我们可以使用文档生成器的 "ListFormat" 属性来开始和结束列表。
# 我们在列表的开始和结束之间添加的每个段落都会成为列表中的一项。
doc_list = doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
# 第一级标签将根据 "Heading 1" 段落样式进行格式化，并带有前缀。
# 这些将显示为 "Appendix A"、"Appendix B"……
doc_list.list_levels[0].number_format = 'Appendix \x00'
doc_list.list_levels[0].number_style = aw.NumberStyle.UPPERCASE_LETTER
doc_list.list_levels[0].linked_style = doc.styles.get_by_name('Heading 1')
# 第二级标签将显示第一和第二列表级别的当前数字，并带有前导零。
# 如果第一级列表为 1，则这些列表标签将显示为 "Section (1.01)"、"Section (1.02)"……
doc_list.list_levels[1].number_format = 'Section (\x00.\x01)'
doc_list.list_levels[1].number_style = aw.NumberStyle.LEADING_ZERO
# 请注意，更高级别使用 UppercaseLetter 编号。
# 我们可以设置 "IsLegal" 属性，以在更高级别使用阿拉伯数字。
doc_list.list_levels[1].is_legal = True
doc_list.list_levels[1].restart_after_level = 0
# 第三级标签将使用大写罗马数字，带有前缀和后缀，并在每个列表第一级项目处重新开始。
# 这些列表标签将显示为 "-I-"、"-II-"……
doc_list.list_levels[2].number_format = '-\x02-'
doc_list.list_levels[2].number_style = aw.NumberStyle.UPPERCASE_ROMAN
doc_list.list_levels[2].restart_after_level = 1
# 将所有列表级别的标签加粗。
for level in doc_list.list_levels:
    level.font.bold = True
# 对当前段落应用列表格式。
builder.list_format.list = doc_list
# 创建列表项，以显示我们所有三个列表级别。
n = 0
while n < 2:
    i = 0
    while i < 3:
        builder.list_format.list_level_number = i
        builder.writeln('Level ' + str(i))
        i += 1
    n += 1
builder.list_format.remove_numbers()
doc.save(file_name=ARTIFACTS_DIR + 'Lists.CreateListRestartAfterHigher.docx')
```

### See Also

* module [aspose.words.lists](../../)
* class [ListLevel](../)

