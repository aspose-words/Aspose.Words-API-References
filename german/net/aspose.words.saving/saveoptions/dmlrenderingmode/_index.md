---
title: SaveOptions.DmlRenderingMode
second_title: Aspose.Words für .NET-API-Referenz
description: SaveOptions eigendom. Ruft einen Wert ab oder legt ihn fest der bestimmt wie DrawingMLFormen gerendert werden.
type: docs
weight: 70
url: /de/net/aspose.words.saving/saveoptions/dmlrenderingmode/
---
## SaveOptions.DmlRenderingMode property

Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie DrawingML-Formen gerendert werden.

```csharp
public DmlRenderingMode DmlRenderingMode { get; set; }
```

### Bemerkungen

Der Standardwert istFallback .

Diese Eigenschaft wird verwendet, wenn das Dokument in feste Seitenformate exportiert wird.

### Beispiele

Zeigt, wie Fallback-Formen beim Speichern in PDF gerendert werden.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft "DmlRenderingMode" auf "DmlRenderingMode.Fallback"
// um DML-Shapes durch ihre Fallback-Shapes zu ersetzen.
// Setzen Sie die Eigenschaft "DmlRenderingMode" auf "DmlRenderingMode.DrawingML"
// um die DML-Formen selbst zu rendern.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

Zeigt, wie die Renderqualität von DrawingML-Effekten in einem Dokument konfiguriert wird, während wir es als PDF speichern.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Legen Sie die Eigenschaft "DmlEffectsRenderingMode" auf "DmlEffectsRenderingMode.None" fest, um alle DrawingML-Effekte zu verwerfen.
// Setzen Sie die Eigenschaft "DmlEffectsRenderingMode" auf "DmlEffectsRenderingMode.Simplified"
// um eine vereinfachte Version von DrawingML-Effekten zu rendern.
// Legen Sie die Eigenschaft "DmlEffectsRenderingMode" auf "DmlEffectsRenderingMode.Fine" fest
// Rendern von DrawingML-Effekten mit größerer Genauigkeit und auch mit höheren Verarbeitungskosten.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Siehe auch

* enum [DmlRenderingMode](../../dmlrenderingmode/)
* class [SaveOptions](../)
* namensraum [Aspose.Words.Saving](../../saveoptions/)
* Montage [Aspose.Words](../../../)


