---
title: TxtSaveOptions.preserve_table_layout property
linktitle: preserve_table_layout property
articleTitle: preserve_table_layout property
second_title: Aspose.Words for Python
description: "TxtSaveOptions.preserve_table_layout property. Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format"
type: docs
weight: 60
url: /zh/python-net/aspose.words.saving/txtsaveoptions/preserve_table_layout/
---

## TxtSaveOptions.preserve_table_layout property

Specifies whether the program should attempt to preserve layout of tables when saving in the plain text format.
The default value is ``False``.



```python
@property
def preserve_table_layout(self) -> bool:
    ...

@preserve_table_layout.setter
def preserve_table_layout(self, value: bool):
    ...

```

### Examples

Shows how to preserve the layout of tables when converting to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.start_table()
builder.insert_cell()
builder.write('Row 1, cell 1')
builder.insert_cell()
builder.write('Row 1, cell 2')
builder.end_row()
builder.insert_cell()
builder.write('Row 2, cell 1')
builder.insert_cell()
builder.write('Row 2, cell 2')
builder.end_table()
# 创建一个 "TxtSaveOptions" 对象，我们可以将其传递给文档的 "Save" 方法
# 以修改我们将文档保存为纯文本的方式。
txt_save_options = aw.saving.TxtSaveOptions()
# 将 "PreserveTableLayout" 属性设置为 "true" 以对内容应用空白填充
# 在输出纯文本文档中，尽可能保留表格布局。
# 将 "PreserveTableLayout" 属性设置为 "false" 以保存所有表格的内容
# 作为连续的文本块，每行仅换行一次。
txt_save_options.preserve_table_layout = preserve_table_layout
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PreserveTableLayout.txt', save_options=txt_save_options)
doc_text = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'TxtSaveOptions.PreserveTableLayout.txt')
if preserve_table_layout:
    self.assertEqual('Row 1, cell 1                                            Row 1, cell 2\r\n' + 'Row 2, cell 1                                            Row 2, cell 2\r\n\r\n', doc_text)
else:
    self.assertEqual('Row 1, cell 1\r' + 'Row 1, cell 2\r' + 'Row 2, cell 1\r' + 'Row 2, cell 2\r\r\n', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptions](../)

