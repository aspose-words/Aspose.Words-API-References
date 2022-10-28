---
title: insert_document method
second_title: Aspose.Words for Python via .NET API Reference
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
| src_doc | [Document](../../document/) |  |
| import_format_mode | [ImportFormatMode](../../importformatmode/) |  |

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
| src_doc | [Document](../../document/) |  |
| import_format_mode | [ImportFormatMode](../../importformatmode/) |  |
| import_format_options | [ImportFormatOptions](../../importformatoptions/) |  |

This method mimics the MS Word behavior, as if CTRL+'A' (select all content) was pressed,
then CTRL+'C' (copy selected into the buffer) inside one document
and then CTRL+'V' (insert content from the buffer) inside another document.


### Returns

First node of the inserted content.


## Examples

Shows how to insert a document into another document.

```python
doc = aw.Document(MY_DIR + "Document.docx")

builder = aw.DocumentBuilder(doc)
builder.move_to_document_end()
builder.insert_break(aw.BreakType.PAGE_BREAK)

doc_to_insert = aw.Document(MY_DIR + "Formatted elements.docx")

builder.insert_document(doc_to_insert, aw.ImportFormatMode.KEEP_SOURCE_FORMATTING)
builder.document.save(ARTIFACTS_DIR + "DocumentBuilder.insert_document.docx")
```

Shows how to resolve duplicate styles while inserting documents.

```python
dst_doc = aw.Document()
builder = aw.DocumentBuilder(dst_doc)

my_style = builder.document.styles.add(aw.StyleType.PARAGRAPH, "MyStyle")
my_style.font.size = 14
my_style.font.name = "Courier New"
my_style.font.color = drawing.Color.blue

builder.paragraph_format.style_name = my_style.name
builder.writeln("Hello world!")

# Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
# If we insert the clone into the original document, the two styles with the same name will cause a clash.
src_doc = dst_doc.clone()
src_doc.styles.get_by_name("MyStyle").font.color = drawing.Color.red

# When we enable "smart_style_behavior" and use the KEEP_SOURCE_FORMATTING import format mode,
# Aspose.Words will resolve style clashes by converting source document styles.
# with the same names as destination styles into direct paragraph attributes.
options = aw.ImportFormatOptions()
options.smart_style_behavior = True

builder.insert_document(src_doc, aw.ImportFormatMode.KEEP_SOURCE_FORMATTING, options)

dst_doc.save(ARTIFACTS_DIR + "DocumentBuilder.smart_style_behavior.docx")
```

## See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

