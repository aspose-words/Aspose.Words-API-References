---
title: TextOutputMode
second_title: Aspose.Words for .NET API Reference
description: SvgSaveOptions property. Gets or sets a value determining how text should be rendered in SVG in C#.
type: docs
weight: 90
url: /net/aspose.words.saving/svgsaveoptions/textoutputmode/
---
## SvgSaveOptions.TextOutputMode property

Gets or sets a value determining how text should be rendered in SVG.

```csharp
public SvgTextOutputMode TextOutputMode { get; set; }
```

## Remarks

Use this property to get or set the mode of how text inside a document should be rendered when saving in SVG format.

The default value is UseTargetMachineFonts.

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

* enum [SvgTextOutputMode](../../svgtextoutputmode/)
* class [SvgSaveOptions](../)
* namespace [Aspose.Words.Saving](../../svgsaveoptions/)
* assembly [Aspose.Words](../../../)
