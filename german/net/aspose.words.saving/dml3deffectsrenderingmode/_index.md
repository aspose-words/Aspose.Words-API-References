---
title: Dml3DEffectsRenderingMode Enum
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie Ihre Dokumente mit der Dml3DEffectsRenderingMode-Aufzählung von Aspose.Words für eine überragende 3D-Formwiedergabe und visuelle Wirkung verbessern können.
type: docs
weight: 5650
url: /de/net/aspose.words.saving/dml3deffectsrenderingmode/
---
## Dml3DEffectsRenderingMode enumeration

Gibt an, wie 3D-Formeffekte gerendert werden.

```csharp
public enum Dml3DEffectsRenderingMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Basic | `0` | Ein leichtes und stabiles Rendering, basierend auf der internen Engine, aber erweiterte Effekte wie Beleuchtung, Materialien und andere zusätzliche Effekte werden in diesem Modus nicht angezeigt. Weitere Informationen finden Sie in der Dokumentation. |
| Advanced | `1` | Rendern einer erweiterten Liste von Spezialeffekten, einschließlich erweiterter 3D-Effekte wie Abschrägungen, Beleuchtung und Materialien. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
