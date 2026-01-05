---
title: DoclingSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words for .NET
description: Specify Docling as the output format when saving documents using DoclingSaveOptions in Aspose.Words.
type: docs
weight: 30
url: /net/aspose.words.saving/doclingsaveoptions/saveformat/
---
## DoclingSaveOptions.SaveFormat property

Specifies the format in which the document will be saved if this save options object is used. Can only be Docling.

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Examples

Shows how to save a document into a Docling JSON format.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

DoclingSaveOptions saveOptions = new DoclingSaveOptions();
saveOptions.SaveFormat = SaveFormat.Docling;
// Set to true to render non-image shapes and include them in the output.
// Set to false (default) to exclude non-image shapes from the output.
saveOptions.RenderNonImageShapes = true;

doc.Save(ArtifactsDir + "DoclingSaveOptions.DoclingJson.json", saveOptions);
```

### See Also

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [DoclingSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
