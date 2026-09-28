---
title: TxtSaveOptions.simplify_list_labels property
linktitle: simplify_list_labels property
articleTitle: simplify_list_labels property
second_title: Aspose.Words for Python
description: "TxtSaveOptions.simplify_list_labels property. Specifies whether the program should simplify list labels in case of complex label formatting not being adequately represented by plain text."
type: docs
weight: 80
url: /zh/python-net/aspose.words.saving/txtsaveoptions/simplify_list_labels/
---

## TxtSaveOptions.simplify_list_labels property

Specifies whether the program should simplify list labels in case of
complex label formatting not being adequately represented by plain text.

If set to ``True``, numbered list labels are written in simple numeric format
and itemized list labels as simple ASCII characters. The default value is ``False``.




```python
@property
def simplify_list_labels(self) -> bool:
    ...

@simplify_list_labels.setter
def simplify_list_labels(self, value: bool):
    ...

```

### Examples

Shows how to change the appearance of lists when saving a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 创建一个有五级缩进的项目符号列表。
builder.list_format.apply_bullet_default()
builder.writeln('Item 1')
builder.list_format.list_indent()
builder.writeln('Item 2')
builder.list_format.list_indent()
builder.writeln('Item 3')
builder.list_format.list_indent()
builder.writeln('Item 4')
builder.list_format.list_indent()
builder.write('Item 5')
# 创建一个 "TxtSaveOptions" 对象，我们可以将其传递给文档的 "Save" 方法
# 以修改我们将文档保存为纯文本的方式。
txt_save_options = aw.saving.TxtSaveOptions()
# 将 "SimplifyListLabels" 属性设置为 "true"，以转换某些列表
# 符号为更简洁的 ASCII 字符，例如 '*', 'o', '+', '>', 等。
# 将 "SimplifyListLabels" 属性设置为 "false"，以尽可能保留原始列表符号。
txt_save_options.simplify_list_labels = simplify_list_labels
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.SimplifyListLabels.txt', save_options=txt_save_options)
doc_text = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'TxtSaveOptions.SimplifyListLabels.txt')
new_line = system_helper.environment.Environment.new_line()
if simplify_list_labels:
    self.assertEqual(f'* Item 1{new_line}' + f'  > Item 2{new_line}' + f'    + Item 3{new_line}' + f'      - Item 4{new_line}' + f'        o Item 5{new_line}', doc_text)
else:
    self.assertEqual(f'· Item 1{new_line}' + f'o Item 2{new_line}' + f'§ Item 3{new_line}' + f'· Item 4{new_line}' + f'o Item 5{new_line}', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptions](../)

