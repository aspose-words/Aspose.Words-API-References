---
title: DocumentBase.PageColor
linktitle: PageColor
second_title: Aspose.Words for .NET API Reference
description: DocumentBase PageColor property. Gets or sets the page color of the document. This property is a simpler version of BackgroundShape in C#.
type: docs
weight: 60
url: /net/aspose.words/documentbase/pagecolor/
---
## PageColor property

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
* namespace [Aspose.Words](../../documentbase/)
* assembly [Aspose.Words](../../../)
