---
title: DocumentBuilder.InsertDocument
linktitle: InsertDocument
second_title: Aspose.Words for .NET API Reference
description: DocumentBuilder method. Inserts a document at the cursor position in C#.
type: docs
weight: 310
url: /net/aspose.words/documentbuilder/insertdocument/
---
## InsertDocument([Document](aspose.words/document/), [ImportFormatMode](aspose.words/importformatmode/)) {#insertdocument}

Inserts a document at the cursor position.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode)
```

| Parameter | Type | Description |
| --- | --- | --- |
| srcDoc | Document | Source document for inserting. |
| importFormatMode | ImportFormatMode | Specifies how to merge style formatting that clashes. |

### Return Value

First node of the inserted content.

## Remarks

This method mimics the MS Word behavior, as if CTRL+'A' (select all content) was pressed, then CTRL+'C' (copy selected into the buffer) inside one document and then CTRL+'V' (insert content from the buffer) inside another document.

## Examples

Shows how to insert a document into another document.

```csharp
Document doc = new Document(MyDir + "Document.docx");

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertBreak(BreakType.PageBreak);

Document docToInsert = new Document(MyDir + "Formatted elements.docx");

builder.InsertDocument(docToInsert, ImportFormatMode.KeepSourceFormatting);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.InsertDocument.docx");
```

### See Also

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertDocument([Document](aspose.words/document/), [ImportFormatMode](aspose.words/importformatmode/), [ImportFormatOptions](aspose.words/importformatoptions/)) {#insertdocument_1}

Inserts a document at the cursor position.

```csharp
public Node InsertDocument(Document srcDoc, ImportFormatMode importFormatMode, 
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

## Examples

Shows how to resolve duplicate styles while inserting documents.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Clone the document and edit the clone's "MyStyle" style, so it is a different color than that of the original.
// If we insert the clone into the original document, the two styles with the same name will cause a clash.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// When we enable SmartStyleBehavior and use the KeepSourceFormatting import format mode,
// Aspose.Words will resolve style clashes by converting source document styles.
// with the same names as destination styles into direct paragraph attributes.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### See Also

* class [Node](../../node/)
* class [Document](../../document/)
* enum [ImportFormatMode](../../importformatmode/)
* class [ImportFormatOptions](../../importformatoptions/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)
