---
title: DocumentBase.PageColor
linktitle: PageColor
articleTitle: PageColor
second_title: Aspose.Words for .NET
description: Discover the DocumentBase PageColor property to easily customize your document's page color. Simplify design with this user-friendly feature!
type: docs
weight: 70
url: /net/aspose.words/documentbase/pagecolor/
---
## DocumentBase.PageColor property

Gets or sets the page color of the document. This property is a simpler version of [`BackgroundShape`](../backgroundshape/).

```csharp
public Color PageColor { get; set; }
```

## Remarks

This property provides a simple way to specify a solid page color for the document. Setting this property creates and sets an appropriate [`BackgroundShape`](../backgroundshape/).

If the page color is not set (e.g. there is no background shape in the document) returns Empty.

## Examples

Shows how to set the background color for all pages of a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.PageColor = System.Drawing.Color.LightGray;

doc.Save(ArtifactsDir + "DocumentBase.SetPageColor.docx");
```

### See Also

* class [DocumentBase](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
