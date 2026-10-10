---
title: TxtListIndentation.character property
linktitle: character property
articleTitle: character property
second_title: Aspose.Words for Python
description: "TxtListIndentation.character property. Gets or sets which character to use for indenting list levels"
type: docs
weight: 20
url: /zh/python-net/aspose.words.saving/txtlistindentation/character/
---

## TxtListIndentation.character property

Gets or sets which character to use for indenting list levels.
The default value is '\\0', that means there is no indentation.


```python
@property
def character(self) -> str:
    ...

@character.setter
def character(self, value: str):
    ...

```

### Examples

Shows how to configure list indenting when saving a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 创建一个具有三级缩进的列表。
builder.list_format.apply_number_default()
builder.writeln('Item 1')
builder.list_format.list_indent()
builder.writeln('Item 2')
builder.list_format.list_indent()
builder.write('Item 3')
# 创建一个 "TxtSaveOptions" 对象，我们可以将其传递给文档的 "Save" 方法
# 以修改我们将文档保存为纯文本的方式。
txt_save_options = aw.saving.TxtSaveOptions()
# 设置 "Character" 属性以指定要使用的字符
# 用于填充，以在纯文本中模拟列表缩进。
txt_save_options.list_indentation.character = ' '
# 设置 "Count" 属性以指定次数
# 在每个列表缩进级别放置填充字符的次数。
txt_save_options.list_indentation.count = 3
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.TxtListIndentation.txt', save_options=txt_save_options)
doc_text = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'TxtSaveOptions.TxtListIndentation.txt')
new_line = system_helper.environment.Environment.new_line()
self.assertEqual(f'1. Item 1{new_line}' + f'   a. Item 2{new_line}' + f'      i. Item 3{new_line}', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtListIndentation](../)

