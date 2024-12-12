---
title: Aspose::Words::DocumentBuilder::InsertDocumentInline method
linktitle: InsertDocumentInline
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBuilder::InsertDocumentInline method. Inserts a document inline at the cursor position in C++.'
type: docs
weight: 33500
url: /cpp/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder::InsertDocumentInline method


Inserts a document inline at the cursor position.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::InsertDocumentInline(const System::SharedPtr<Aspose::Words::Document> &srcDoc, Aspose::Words::ImportFormatMode importFormatMode, const System::SharedPtr<Aspose::Words::ImportFormatOptions> &importFormatOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | const System::SharedPtr\<Aspose::Words::Document\>\& | Source document for inserting. |
| importFormatMode | Aspose::Words::ImportFormatMode | Specifies how to merge style formatting that clashes. |
| importFormatOptions | const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\& | Allows to specify options that affect formatting of a result document. |

### ReturnValue

First node of the inserted content.
## Remarks


This method mimics the MS Word behavior, as if CTRL+'A' (select all content) was pressed, then CTRL+'C' (copy selected into the buffer) inside one document and then CTRL+'V' (insert content from the buffer) inside another document.

As a difference from [InsertDocument()](../) this method moves the content of the paragraph of the destination document, before which the source document is inserted, into the last paragraph of the inserted source document. Actually, this means that paragraph break of the last inserted paragraph is removed.

Note, if the last node of the source document is not a paragraph, then nothing will be done.

## See Also

* Class [Node](../../node/)
* Class [Document](../../document/)
* Enum [ImportFormatMode](../../importformatmode/)
* Class [ImportFormatOptions](../../importformatoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
