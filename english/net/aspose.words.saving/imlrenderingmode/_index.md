---
title: ImlRenderingMode Enum
linktitle: ImlRenderingMode
second_title: Aspose.Words for .NET API Reference
description: Aspose.Words.Saving.ImlRenderingMode enum. Specifies how ink InkML objects are rendered to fixed page formats in C#.
type: docs
weight: 5030
url: /net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

Specifies how ink (InkML) objects are rendered to fixed page formats.

```csharp
public enum ImlRenderingMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Fallback | `0` | If fall-back shape is available for ink (InkML) object, Aspose.Words renders fall-back shape instead of the InkML. |
| InkML | `1` | Aspose.Words ignores fall-back shape of ink (InkML) object and renders InkML itself. This is the default mode. |

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
