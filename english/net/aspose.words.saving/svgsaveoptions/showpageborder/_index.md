---
title: SvgSaveOptions.ShowPageBorder
linktitle: ShowPageBorder
articleTitle: ShowPageBorder
second_title: Aspose.Words for .NET
description: Discover the SvgSaveOptions ShowPageBorder property to customize your page outline. Control borders effortlessly—default setting is true for easy use!
type: docs
weight: 110
url: /net/aspose.words.saving/svgsaveoptions/showpageborder/
---
## SvgSaveOptions.ShowPageBorder property

Controls whether a border is added to the outline of the page. Default is `true`.

```csharp
public bool ShowPageBorder { get; set; }
```

## Examples

Shows how to mimic the properties of images when converting a .docx document to .svg.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Configure the SvgSaveOptions object to save with no page borders or selectable text.
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### See Also

* class [SvgSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
