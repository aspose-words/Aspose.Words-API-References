---
title: ImportFormatOptions.keep_source_numbering property
linktitle: keep_source_numbering property
articleTitle: keep_source_numbering property
second_title: Aspose.Words for Python
description: "ImportFormatOptions.keep_source_numbering property. Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and destination documents"
type: docs
weight: 70
url: /zh/python-net/aspose.words/importformatoptions/keep_source_numbering/
---

## ImportFormatOptions.keep_source_numbering property

Gets or sets a boolean value that specifies how the numbering will be imported when it clashes in source and
destination documents.
The default value is ``False``.



```python
@property
def keep_source_numbering(self) -> bool:
    ...

@keep_source_numbering.setter
def keep_source_numbering(self, value: bool):
    ...

```

### Examples

Shows how to import a document with numbered lists.

```python
src_doc = aw.Document(file_name=MY_DIR + 'List source.docx')
dst_doc = aw.Document(file_name=MY_DIR + 'List destination.docx')
self.assertEqual(4, dst_doc.lists.count)
options = aw.ImportFormatOptions()
# 如果列表样式冲突，应用源文档的列表格式。
# 将 "KeepSourceNumbering" 属性设置为 "false"，以不将任何列表编号导入目标文档。
# 将 "KeepSourceNumbering" 属性设置为 "true" 以导入所有冲突项。
# 列表样式编号保持与源文档中相同的外观。
options.keep_source_numbering = is_keep_source_numbering
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=options)
dst_doc.update_list_labels()
self.assertEqual(5 if is_keep_source_numbering else 4, dst_doc.lists.count)
```

Shows how resolve a clash when importing documents that have lists with the same list definition identifier.

```python
src_doc = aw.Document(file_name=MY_DIR + 'List with the same definition identifier - source.docx')
dst_doc = aw.Document(file_name=MY_DIR + 'List with the same definition identifier - destination.docx')
# 将 "KeepSourceNumbering" 属性设置为 "true"，以应用不同的列表定义 ID
# 以匹配 Aspose.Words 将其导入目标文档时的相同样式。
import_format_options = aw.ImportFormatOptions()
import_format_options.keep_source_numbering = True
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.USE_DESTINATION_STYLES, import_format_options=import_format_options)
dst_doc.update_list_labels()
```

Shows how to resolve list numbering clashes in source and destination documents.

```python
# 打开一个具有自定义列表编号方案的文档，然后克隆它。
# 由于两者具有相同的编号格式，如果我们将一个文档导入另一个文档，格式将冲突。
src_doc = aw.Document(file_name=MY_DIR + 'Custom list numbering.docx')
dst_doc = src_doc.clone()
# 当我们将文档的克隆导入原始文档并随后追加时，
# 则具有相同列表格式的两个列表将合并。
# 如果我们将 "KeepSourceNumbering" 标志设置为 "false"，则来自文档克隆的列表
# 我们追加到原始文档的列表将继续使用我们追加到的列表的编号。
# 这将有效地将两个列表合并为一个。
# 如果我们将 "KeepSourceNumbering" 标志设置为 "true"，则文档克隆
# 列表将保留其原始编号，使两个列表显示为独立的列表。
import_format_options = aw.ImportFormatOptions()
import_format_options.keep_source_numbering = keep_source_numbering
importer = aw.NodeImporter(src_doc=src_doc, dst_doc=dst_doc, import_format_mode=aw.ImportFormatMode.KEEP_DIFFERENT_STYLES, import_format_options=import_format_options)
for paragraph in src_doc.first_section.body.paragraphs:
    paragraph = paragraph.as_paragraph()
    imported_node = importer.import_node(paragraph, True)
    dst_doc.first_section.body.append_child(imported_node)
dst_doc.update_list_labels()
if keep_source_numbering:
    self.assertEqual('6. Item 1\r\n' + '7. Item 2 \r\n' + '8. Item 3\r\n' + '9. Item 4\r\n' + '6. Item 1\r\n' + '7. Item 2 \r\n' + '8. Item 3\r\n' + '9. Item 4', dst_doc.first_section.body.to_string(save_format=aw.SaveFormat.TEXT).strip())
else:
    self.assertEqual('6. Item 1\r\n' + '7. Item 2 \r\n' + '8. Item 3\r\n' + '9. Item 4\r\n' + '10. Item 1\r\n' + '11. Item 2 \r\n' + '12. Item 3\r\n' + '13. Item 4', dst_doc.first_section.body.to_string(save_format=aw.SaveFormat.TEXT).strip())
```

### See Also

* module [aspose.words](../../)
* class [ImportFormatOptions](../)

