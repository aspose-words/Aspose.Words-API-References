---
title: SaveOptions.ImlRenderingMode
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words for .NET
description: Discover how the SaveOptions ImlRenderingMode property enhances InkML object rendering. Optimize your ink rendering for better visual results!
type: docs
weight: 90
url: /net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

Gets or sets a value determining how ink (InkML) objects are rendered.

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

## Remarks

The default value is InkML.

This property is used when the document is exported to fixed page formats.

## Examples

Shows how to render Ink object.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Set 'ImlRenderingMode.InkML' ignores fall-back shape of ink (InkML) object and renders InkML itself.
// If the rendering result is unsatisfactory,
// please use 'ImlRenderingMode.Fallback' to get a result similar to previous versions.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### See Also

* enum [ImlRenderingMode](../../imlrenderingmode/)
* class [SaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
