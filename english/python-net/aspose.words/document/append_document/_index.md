---
title: Document.append_document method
linktitle: append_document method
articleTitle: append_document method
second_title: Aspose.Words for Python
description: "aspose.words.Document.append_document method"
type: docs
weight: 570
url: /python-net/aspose.words/document/append_document/
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
# Append the source document to the destination document while preserving its formatting,
# then save the source document to the local file system.
dst_doc.append_document(src_doc, aw.ImportFormatMode.KEEP_SOURCE_FORMATTING)
dst_doc.save(ARTIFACTS_DIR + 'Document.append_document.docx')
```

Shows how to append all the documents in a folder to the end of a template document.

```python
dst_doc = aw.Document()
builder = aw.DocumentBuilder(dst_doc)
builder.paragraph_format.style_identifier = aw.StyleIdentifier.HEADING1
builder.writeln('Template Document')
builder.paragraph_format.style_identifier = aw.StyleIdentifier.NORMAL
builder.writeln('Some content here')
# Append all unencrypted documents with the .doc extension
# from our local file system directory to the base document.
doc_files = glob.glob(MY_DIR + '*.doc')
for file_name in doc_files:
    info = aw.FileFormatUtil.detect_file_format(file_name)
    if info.is_encrypted:
        continue
    src_doc = aw.Document(file_name)
    dst_doc.append_document(src_doc, aw.ImportFormatMode.USE_DESTINATION_STYLES)
dst_doc.save(ARTIFACTS_DIR + 'Document.append_all_documents_in_folder.doc')
```

Shows how to manage list style clashes while appending a document.

```python
# Load a document with text in a custom style and clone it.
src_doc = aw.Document(file_name=MY_DIR + 'Custom list numbering.docx')
dst_doc = src_doc.clone()
# We now have two documents, each with an identical style named "CustomStyle".
# Change the text color for one of the styles to set it apart from the other.
dst_doc.styles.get_by_name('CustomStyle').font.color = aspose.pydrawing.Color.dark_red
# If there is a clash of list styles, apply the list format of the source document.
# Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
# Set the "KeepSourceNumbering" property to "true" import all clashing
# list style numbering with the same appearance that it had in the source document.
options = aw.ImportFormatOptions()
options.keep_source_numbering = keep_source_numbering
# Joining two documents that have different styles that share the same name causes a style clash.
# We can specify an import format mode while appending documents to resolve this clash.
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
list = dst_doc.lists[0]
builder.list_format.list = list
i = 1
while i <= 15:
    builder.write(f'List Item {i}\n')
    i += 1
attach_doc = dst_doc.clone(True).as_document()
# If there is a clash of list styles, apply the list format of the source document.
# Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
# Set the "KeepSourceNumbering" property to "true" import all clashing
# list style numbering with the same appearance that it had in the source document.
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
# If there is a clash of list styles, apply the list format of the source document.
# Set the "KeepSourceNumbering" property to "false" to not import any list numbers into the destination document.
# Set the "KeepSourceNumbering" property to "true" import all clashing
# list style numbering with the same appearance that it had in the source document.
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

