---
title: SaveOptions.Dml3DEffectsRenderingMode
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SaveOptions Dml3DEffectsRenderingMode för att enkelt styra 3D-effektrendering för förbättrad visuell kvalitet i dina applikationer.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/saveoptions/dml3deffectsrenderingmode/
---
## SaveOptions.Dml3DEffectsRenderingMode property

Hämtar eller ställer in ett värde som avgör hur 3D-effekter renderas.

```csharp
public Dml3DEffectsRenderingMode Dml3DEffectsRenderingMode { get; set; }
```

## Anmärkningar

Standardvärdet ärBasic .

## Exempel

Visar hur 3D-effekter återges.

```csharp
Document doc = new Document(MyDir + "DrawingML shape 3D effects.docx");

RenderCallback warningCallback = new RenderCallback();
doc.WarningCallback = warningCallback;

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced;

doc.Save(ArtifactsDir + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
```

### Se även

* enum [Dml3DEffectsRenderingMode](../../dml3deffectsrenderingmode/)
* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
