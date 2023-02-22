---
title: Enum DmlRenderingMode
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.DmlRenderingMode opsomming. Gibt an wie DrawingMLFormen in feste Seitenformate gerendert werden.
type: docs
weight: 4660
url: /de/net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

Gibt an, wie DrawingML-Formen in feste Seitenformate gerendert werden.

```csharp
public enum DmlRenderingMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Fallback | `0` | Wenn die Fallback-Form für DrawingML verfügbar ist, rendert Aspose.Words die Fallback-Form anstelle von DrawingML. |
| DrawingML | `1` | Aspose.Words ignoriert die Fallback-Form von DrawingML und rendert DrawingML selbst. Dies ist der Standardmodus. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)


