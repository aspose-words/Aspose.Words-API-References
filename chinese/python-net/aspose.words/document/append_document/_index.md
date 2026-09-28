---
title: Document.append_document method
linktitle: append_document method
articleTitle: append_document method
second_title: Aspose.Words for Python
description: "aspose.words.Document.append_document method"
type: docs
weight: 580
url: /zh/python-net/aspose.words/document/append_document/
---

## append_document(src_doc, import_format_mode) {#document_importformatmode}

Appends the specified document to the end of this document.


```python
def append_document(self, src_doc: aspose.words.Document, import_format_mode: aspose.words.ImportFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_doc | [Document](../) | The document to append. |
| import_format_mode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |

## append_document(src_doc, import_format_mode, import_format_options) {#document_importformatmode_importformatoptions}

Appends the specified document to the end of this document.


```python
def append_document(self, src_doc: aspose.words.Document, import_format_mode: aspose.words.ImportFormatMode, import_format_options: aspose.words.ImportFormatOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_doc | [Document](../) | The document to append. |
| import_format_mode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |
| import_format_options | [ImportFormatOptions](../../importformatoptions/) | Allows to specify options that affect formatting of a result document. |

## Examples

Shows how to append a document to the end of another document.

```python
src_doc = aw.Document()
src_doc.first_section.body.append_paragraph('Source document text. ')
dst_doc = aw.Document()
dst_doc.first_section.body.append_paragraph('Destination document text. ')
# 在保留源文档格式的情况下，将源文档追加到目标文档，
# 然后将源文档保存到本地文件系统。
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING)
dst_doc.save(file_name=ARTIFACTS_DIR + 'Document.AppendDocument.docx')
```

Shows how to append all the documents in a folder to the end of a template document.

```python
dst_doc = aw.Document()
builder = aw.DocumentBuilder(doc=dst_doc)
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Template Document')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.writeln('Some content here')
# 追加所有未加密的 .doc 扩展名文档
# 从我们的本地文件系统目录追加到基文档。
doc_files = list(filter(lambda item: item.endswith('.doc'), list(system_helper.io.Directory.get_files(MY_DIR, '*.doc'))))
for file_name in doc_files:
    info = aw.FileFormatUtil.detect_file_format(file_name=file_name)
    if info.is_encrypted:
        continue
    src_doc = aw.Document(file_name=file_name)
    dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.USE_DESTINATION_STYLES)
dst_doc.save(file_name=ARTIFACTS_DIR + 'Document.AppendAllDocumentsInFolder.doc')
```

Shows how to manage list style clashes while appending a document.

```python
# 加载一个使用自定义样式的文档并克隆它。
src_doc = aw.Document(file_name=MY_DIR + 'Custom list numbering.docx')
dst_doc = src_doc.clone()
# 我们现在有两个文档，每个文档都有名为 "CustomStyle" 的相同样式。
# 更改其中一种样式的文字颜色，以使其区别于另一种。
dst_doc.styles.get_by_name('CustomStyle').font.color = aspose.pydrawing.Color.dark_red
# 如果列表样式冲突，应用源文档的列表格式。
# 将 "KeepSourceNumbering" 属性设置为 "false"，以不将任何列表编号导入目标文档。
# 将 "KeepSourceNumbering" 属性设置为 "true" 以导入所有冲突项。
# 列表样式编号保持与源文档中相同的外观。
options = aw.ImportFormatOptions()
options.keep_source_numbering = keep_source_numbering
# 合并两个具有不同样式但名称相同的文档会导致样式冲突。
# 我们可以在追加文档时指定导入格式模式以解决此冲突。
dst_doc.append_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.KEEP_DIFFERENT_STYLES, import_format_options=options)
dst_doc.update_list_labels()
dst_doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.AppendDocumentAndResolveStyles.docx')
```

Shows how to manage list style clashes while inserting a document.

```python
dst_doc = aw.Document()
builder = aw.DocumentBuilder(doc=dst_doc)
builder.insert_break(aw.BreakType.PARAGRAPH_BREAK)
dst_doc.lists.add(list_template=aw.lists.ListTemplate.NUMBER_DEFAULT)
doc_list = dst_doc.lists[0]
builder.list_format.list = doc_list
i = 1
while i <= 15:
    builder.write(f'List Item {i}\n')
    i += 1
attach_doc = dst_doc.clone(True).as_document()
# 如果列表样式冲突，应用源文档的列表格式。
# 将 "KeepSourceNumbering" 属性设置为 "false"，以不将任何列表编号导入目标文档。
# 将 "KeepSourceNumbering" 属性设置为 "true" 以导入所有冲突项。
# 列表样式编号保持与源文档中相同的外观。
import_options = aw.ImportFormatOptions()
import_options.keep_source_numbering = keep_source_numbering
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.insert_document(src_doc=attach_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=import_options)
dst_doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertDocumentAndResolveStyles.docx')
```

Shows how to manage list style clashes while appending a clone of a document to itself.

```python
src_doc = aw.Document(file_name=MY_DIR + 'List item.docx')
dst_doc = aw.Document(file_name=MY_DIR + 'List item.docx')
# 如果列表样式冲突，应用源文档的列表格式。
# 将 "KeepSourceNumbering" 属性设置为 "false"，以不将任何列表编号导入目标文档。
# 将 "KeepSourceNumbering" 属性设置为 "true" 以导入所有冲突项。
# 列表样式编号保持与源文档中相同的外观。
builder = aw.DocumentBuilder(doc=dst_doc)
builder.move_to_document_end()
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
options = aw.ImportFormatOptions()
options.keep_source_numbering = keep_source_numbering
builder.insert_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=options)
dst_doc.update_list_labels()
```

## See Also

* module [aspose.words](../../)
* class [Document](../)

