﻿---
title: DocumentBuilder.insert_document method
linktitle: insert_document method
articleTitle: insert_document method
second_title: Aspose.Words for Python
description: "aspose.words.DocumentBuilder.insert_document method"
type: docs
weight: 310
url: /python-net/aspose.words/documentbuilder/insert_document/
---

## insert_document(src_doc, import_format_mode) {#document_importformatmode}

Inserts a document at the cursor position.


```python
def insert_document(self, src_doc: aspose.words.Document, import_format_mode: aspose.words.ImportFormatMode):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_doc | [Document](../../document/) | Source document for inserting. |
| import_format_mode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |

### Remarks

This method mimics the MS Word behavior, as if CTRL+'A' (select all content) was pressed,
then CTRL+'C' (copy selected into the buffer) inside one document
and then CTRL+'V' (insert content from the buffer) inside another document.


### Returns

First node of the inserted content.


## insert_document(src_doc, import_format_mode, import_format_options) {#document_importformatmode_importformatoptions}

Inserts a document at the cursor position.


```python
def insert_document(self, src_doc: aspose.words.Document, import_format_mode: aspose.words.ImportFormatMode, import_format_options: aspose.words.ImportFormatOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| src_doc | [Document](../../document/) | Source document for inserting. |
| import_format_mode | [ImportFormatMode](../../importformatmode/) | Specifies how to merge style formatting that clashes. |
| import_format_options | [ImportFormatOptions](../../importformatoptions/) | Allows to specify options that affect formatting of a result document. |

### Remarks

This method mimics the MS Word behavior, as if CTRL+'A' (select all content) was pressed,
then CTRL+'C' (copy selected into the buffer) inside one document
and then CTRL+'V' (insert content from the buffer) inside another document.


### Returns

First node of the inserted content.


## Examples

Shows how to insert a document into another document.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_document_end()
builder.insert_break(aw.BreakType.PAGE_BREAK)
doc_to_insert = aw.Document(file_name=MY_DIR + 'Formatted elements.docx')
builder.insert_document(src_doc=doc_to_insert, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING)
builder.document.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.InsertDocument.docx')
```

Shows how to resolve duplicate styles while inserting documents.

```python
dst_doc = aw.Document()
builder = aw.DocumentBuilder(doc=dst_doc)
my_style = builder.document.styles.add(aw.StyleType.PARAGRAPH, 'MyStyle')
my_style.font.size = 14
my_style.font.name = 'Courier New'
my_style.font.color = aspose.pydrawing.Color.blue
builder.paragraph_format.style_name = my_style.name
builder.writeln('Hello world!')
# Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
# If we insert the clone into the original document, the two styles with the same name will cause a clash.
src_doc = dst_doc.clone()
src_doc.styles.get_by_name('MyStyle').font.color = aspose.pydrawing.Color.red
# When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
# Aspose.Words will resolve style clashes by converting source document styles.
# with the same names as destination styles into direct paragraph attributes.
options = aw.ImportFormatOptions()
options.smart_style_behavior = True
builder.insert_document(src_doc=src_doc, import_format_mode=aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, import_format_options=options)
dst_doc.save(file_name=ARTIFACTS_DIR + 'DocumentBuilder.SmartStyleBehavior.docx')
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

