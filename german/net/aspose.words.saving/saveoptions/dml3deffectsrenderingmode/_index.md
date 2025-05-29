---
title: SaveOptions.Dml3DEffectsRenderingMode
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die SaveOptions Dml3DEffectsRenderingMode-Eigenschaft, um die 3D-Effektwiedergabe für eine verbesserte visuelle Qualität in Ihren Anwendungen einfach zu steuern.
type: docs
weight: 50
url: /de/net/aspose.words.saving/saveoptions/dml3deffectsrenderingmode/
---
## SaveOptions.Dml3DEffectsRenderingMode property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie 3D-Effekte gerendert werden.

```csharp
public Dml3DEffectsRenderingMode Dml3DEffectsRenderingMode { get; set; }
```

## Bemerkungen

Der Standardwert istBasic .

## Beispiele

Zeigt, wie 3D-Effekte gerendert werden.

```csharp
Document doc = new Document(MyDir + "DrawingML shape 3D effects.docx");

RenderCallback warningCallback = new RenderCallback();
doc.WarningCallback = warningCallback;

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced;

doc.Save(ArtifactsDir + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
```

### Siehe auch

* enum [Dml3DEffectsRenderingMode](../../dml3deffectsrenderingmode/)
* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
