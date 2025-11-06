---
title: Dml3DEffectsRenderingMode Enum
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words for .NET
description: Discover how to enhance your documents with Aspose.Words' Dml3DEffectsRenderingMode enum for superior 3D shape rendering and visual impact.
type: docs
weight: 5690
url: /net/aspose.words.saving/dml3deffectsrenderingmode/
---
## Dml3DEffectsRenderingMode enumeration

Specifies how 3D shape effects are rendered.

```csharp
public enum Dml3DEffectsRenderingMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Basic | `0` | A lightweight and stable rendering, based on the internal engine, but advanced effects such as lighting, materials and other additional effects are not displayed when using this mode. Please see documentation for details. |
| Advanced | `1` | Rendering of an extended list of special effects including advanced 3D effects such as bevels, lighting and materials. |

## Examples

Shows how 3D effects are rendered.

```csharp
Document doc = new Document(MyDir + "DrawingML shape 3D effects.docx");

RenderCallback warningCallback = new RenderCallback();
doc.WarningCallback = warningCallback;

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced;

doc.Save(ArtifactsDir + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
