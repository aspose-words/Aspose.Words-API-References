---
title: DocumentBuilder.InsertDocumentInline
linktitle: InsertDocumentInline
articleTitle: InsertDocumentInline
second_title: Aspose.Words for .NET
description: Effortlessly insert documents inline with the DocumentBuilder InsertDocumentInline method, enhancing your workflow and document editing experience.
type: docs
weight: 320
url: /net/aspose.words/documentbuilder/insertdocumentinline/
---
## DocumentBuilder.InsertDocumentInline method

Inserts a document inline at the cursor position.

```csharp
public Node InsertDocumentInline(Document srcDoc, ImportFormatMode importFormatMode, 
    ImportFormatOptions importFormatOptions)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | Document | Source document for inserting. |
| importFormatMode | ImportFormatMode | Specifies how to merge style formatting that clashes. |
| importFormatOptions | ImportFormatOptions | Allows to specify options that affect formatting of a result document. |

### Return Value

First node of the inserted content.

## Remarks

This method mimics the MS Word behavior, as if CTRL+'A' (select all content) was pressed, then CTRL+'C' (copy selected into the buffer) inside one document and then CTRL+'V' (insert content from the buffer) inside another document.

As a difference from [`InsertDocument`](../insertdocument/) this method moves the content of the paragraph of the destination document, before which the source document is inserted, into the last paragraph of the inserted source document. Actually, this means that paragraph break of the last inserted paragraph is removed.

Note, if the last node of the source document is not a paragraph, then nothing will be done.

## Examples

Shows how to insert a document inline at the cursor position.

```csharp
DocumentBuilder srcDoc = new DocumentBuilder();
srcDoc.Write("[src content]");

// Create destination document.
DocumentBuilder dstDoc = new DocumentBuilder();
dstDoc.Write("Before ");
dstDoc.InsertNode(new BookmarkStart(dstDoc.Document, "src_place"));
dstDoc.InsertNode(new BookmarkEnd(dstDoc.Document, "src_place"));
dstDoc.Write(" after");

Assert.AreEqual("Before  after", dstDoc.Document.GetText().TrimEnd());

// Insert source document into destination inline.
dstDoc.MoveToBookmark("src_place");
dstDoc.InsertDocumentInline(srcDoc.Document, ImportFormatMode.UseDestinationStyles, new ImportFormatOptions());

Assert.AreEqual("Before [src content] after", dstDoc.Document.GetText().TrimEnd());
```

### See Also

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
