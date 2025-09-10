---
title: ImportFormatMode enumeration
linktitle: ImportFormatMode enumeration
articleTitle: ImportFormatMode enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.ImportFormatMode enumeration. Specifies how formatting is merged when importing content from another document."
type: docs
weight: 630
url: /nodejs-net/aspose.words/importformatmode/
---

## ImportFormatMode enumeration

Specifies how formatting is merged when importing content from another document.

When you copy nodes from one document to another, this option specifies how formatting
is resolved when both documents have a style with the same name, but different formatting.

The formatting is resolved as follows:


1. Built-in styles are matched using their locale independent style identifier.
   User defined styles are matched using case-sensitive style name.
   
1. If a matching style is not found in the destination document, the style
   (and all styles referenced by it) are copied into the destination document
   and the imported nodes are updated to reference the new style.
   
1. If a matching style already exists in the destination document, what happens
   depends on the ``importFormatMode`` parameter passed to
   [DocumentBase.importNode()](../documentbase/importNode/#node_boolean_importformatmode)
   as described below.
   
When using the [ImportFormatMode.UseDestinationStyles](./#UseDestinationStyles) option, if a matching style already exists
in the destination document, the style is not copied and the imported nodes are updated
to reference the existing style.

The drawback of using [ImportFormatMode.UseDestinationStyles](./#UseDestinationStyles) is that the imported text might
look different in the destination document comparing to the source document.
For example, the "Heading 1" style in the source document uses Arial 16pt font and
the "Heading 1" style in the destination document uses Times New Roman 14pt font.
When importing text of "Heading 1" style with no other direct formatting, it will
appear as Times New Roman 14pt font in the destination document.

[ImportFormatMode.KeepSourceFormatting](./#KeepSourceFormatting) option allows to make sure the imported content looks the same 
in the destination document like it looks in the source document.
If a matching style already exists in the destination document, the source style formatting is expanded
into direct Node attributes and the style is changed to Normal.
If the style does not exist in the destination document, then the source style is imported
into the destination document and applied to the imported node.
Note, that it is not always possible to preserve the source style even if it does not exist in the destination document.
In this case formatting of such style will be expanded into direct Node attributes in favor of preserving original Node formatting.

The drawback of using [ImportFormatMode.KeepSourceFormatting](./#KeepSourceFormatting) is that if you perform several imports,
you could end up with many styles in the destination document and that could make using
consistent style formatting in Microsoft Word difficult for this document.

Using [ImportFormatMode.KeepDifferentStyles](./#KeepDifferentStyles) option allows to reuse destination styles
if the formatting they provide is identical to the styles in the source document.
If the style in destination document is different from the source then it is imported.




### Members

| Name | Description |
| --- | --- |
| UseDestinationStyles | Use the destination document styles and copy new styles. This is the default option. |
| KeepSourceFormatting | Copy all required styles to the destination document, generate unique style names if needed. |
| KeepDifferentStyles | Only copy styles that are different from those in the source document. |

### Examples

Shows how to insert a document into another document.

```js
let doc = new aw.Document(base.myDir + "Document.docx");

let builder = new aw.DocumentBuilder(doc);
builder.moveToDocumentEnd();
builder.insertBreak(aw.BreakType.PageBreak);

let docToInsert = new aw.Document(base.myDir + "Formatted elements.docx");

builder.insertDocument(docToInsert, aw.ImportFormatMode.KeepSourceFormatting);
builder.document.save(base.artifactsDir + "DocumentBuilder.insertDocument.docx");
```

### See Also

* module [Aspose.Words](../)
* method [DocumentBase.importNode()](../documentbase/importNode/#node_boolean_importformatmode)

