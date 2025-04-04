---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Saving.SvgTextOutputMode enum to customize text rendering in SVG format, enhancing document presentation and visual appeal.
type: docs
weight: 6390
url: /net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

Allows to specify how text inside a document should be rendered when saving in SVG format.

```csharp
public enum SvgTextOutputMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| UseSvgFonts | `0` | SVG fonts are used to render text. Note, not all browsers support SVG fonts. |
| UseTargetMachineFonts | `1` | Fonts installed on the target machine are used to render text. Note, if some of fonts used in the document are not available on the target machine, document can look differently. |
| UsePlacedGlyphs | `2` | Text is rendered using curves. Note, text selection will not work if you use this option. |

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
