---
title: DocumentBuilder.insert_document_inline method
linktitle: insert_document_inline method
articleTitle: insert_document_inline method
second_title: Aspose.Words for Python
description: "DocumentBuilder.insert_document_inline method. Inserts a document inline at the cursor position."
type: docs
weight: 320
url: /python-net/aspose.words/documentbuilder/insert_document_inline/
---

## insert_document_inline(src_doc, import_format_mode, import_format_options) {#document_importformatmode_importformatoptions}

Inserts a document inline at the cursor position.


```python
def insert_document_inline(self, src_doc: aspose.words.Document, import_format_mode: aspose.words.ImportFormatMode, import_format_options: aspose.words.ImportFormatOptions):
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

As a difference from [DocumentBuilder.insert_document()](../insert_document/#document_importformatmode_importformatoptions)
this method moves the content of the paragraph of the destination document,
before which the source document is inserted, into the last
paragraph of the inserted source document. Actually, this means that
paragraph break of the last inserted paragraph is removed.

Note, if the last node of the source document is not a paragraph, then nothing will be done.




### Returns

First node of the inserted content.


### Examples

Shows how to insert a document inline at the cursor position.

```python
src_doc = aw.DocumentBuilder()
src_doc.write('[src content]')
# Create destination document.
dst_doc = aw.DocumentBuilder()
dst_doc.write('Before ')
dst_doc.insert_node(aw.BookmarkStart(dst_doc.document, 'src_place'))
dst_doc.insert_node(aw.BookmarkEnd(dst_doc.document, 'src_place'))
dst_doc.write(' after')
self.assertEqual('Before  after', dst_doc.document.get_text().rstrip())
# Insert source document into destination inline.
dst_doc.move_to_bookmark(bookmark_name='src_place')
dst_doc.insert_document_inline(src_doc.document, aw.ImportFormatMode.USE_DESTINATION_STYLES, aw.ImportFormatOptions())
self.assertEqual('Before [src content] after', dst_doc.document.get_text().rstrip())
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

