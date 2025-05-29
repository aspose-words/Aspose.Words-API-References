---
title: SaveOptions.DmlRenderingMode
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die SaveOptions DmlRenderingMode-Eigenschaft die Darstellung Ihrer DrawingML-Formen verbessert. Optimieren Sie mühelos die visuelle Darstellung Ihrer Dokumente!
type: docs
weight: 70
url: /de/net/aspose.words.saving/saveoptions/dmlrenderingmode/
---
## SaveOptions.DmlRenderingMode property

Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie DrawingML-Formen gerendert werden.

```csharp
public DmlRenderingMode DmlRenderingMode { get; set; }
```

## Bemerkungen

Der Standardwert istFallback .

Diese Eigenschaft wird verwendet, wenn das Dokument in feste Seitenformate exportiert wird.

## Beispiele

Zeigt, wie beim Speichern im PDF-Format Fallback-Formen gerendert werden.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „DmlRenderingMode“ auf „DmlRenderingMode.Fallback“
// um DML-Formen durch ihre Fallback-Formen zu ersetzen.
// Setzen Sie die Eigenschaft „DmlRenderingMode“ auf „DmlRenderingMode.DrawingML“
// um die DML-Formen selbst zu rendern.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

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

* enum [DmlRenderingMode](../../dmlrenderingmode/)
* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
