---
title: SaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SaveOptions DmlEffectsRenderingMode-Eigenschaft die Darstellung von DrawingML-Effekten optimiert, um die Dokumentqualität und Leistung zu verbessern.
type: docs
weight: 60
url: /de/net/aspose.words.saving/saveoptions/dmleffectsrenderingmode/
---
## SaveOptions.DmlEffectsRenderingMode property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie DrawingML-Effekte gerendert werden.

```csharp
public virtual DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## Bemerkungen

Der Standardwert istSimplified .

Diese Eigenschaft wird verwendet, wenn das Dokument in feste Seitenformate exportiert wird.

## Beispiele

Zeigt, wie die Rendering-Qualität von DrawingML-Effekten in einem Dokument beim Speichern im PDF-Format konfiguriert wird.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „DmlEffectsRenderingMode“ auf „DmlEffectsRenderingMode.None“, um alle DrawingML-Effekte zu verwerfen.
// Setzen Sie die Eigenschaft „DmlEffectsRenderingMode“ auf „DmlEffectsRenderingMode.Simplified“
// um eine vereinfachte Version der DrawingML-Effekte zu rendern.
// Setzen Sie die Eigenschaft "DmlEffectsRenderingMode" auf "DmlEffectsRenderingMode.Fine" auf
// DrawingML-Effekte mit höherer Genauigkeit und auch mit höheren Verarbeitungskosten rendern.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Siehe auch

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
