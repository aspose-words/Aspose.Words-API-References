---
title: DoclingSaveOptions.RenderNonImageShapes
linktitle: RenderNonImageShapes
articleTitle: RenderNonImageShapes
second_title: Aspose.Words for .NET
description: DoclingSaveOptions RenderNonImageShapes property. Gets or sets a value indicating whether nonimage shapes should be rendered and written to the output Docling JSON document.
type: docs
weight: 20
url: /net/aspose.words.saving/doclingsaveoptions/rendernonimageshapes/
---
## DoclingSaveOptions.RenderNonImageShapes property

Gets or sets a value indicating whether non-image shapes should be rendered and written to the output Docling JSON document.

```csharp
public bool RenderNonImageShapes { get; set; }
```

## Remarks

If the property is **false**, non-image shapes are not exported to the output document. The default value is **false**.

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

* class [DoclingSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
