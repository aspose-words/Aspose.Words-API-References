---
title: DmlEffectsRenderingMode Enum
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aspose.Words DmlEffectsRenderingMode-Aufzählung für optimiertes DrawingML-Effekt-Rendering in festen Seitenformaten. Verbessern Sie die Qualität Ihrer Dokumente!
type: docs
weight: 5660
url: /de/net/aspose.words.saving/dmleffectsrenderingmode/
---
## DmlEffectsRenderingMode enumeration

Gibt an, wie DrawingML-Effekte in feste Seitenformate gerendert werden.

```csharp
public enum DmlEffectsRenderingMode
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Simplified | `0` | Das Rendern von DrawingML-Effekten wird vereinfacht. |
| None | `1` | Es werden keine DrawingML-Effekte gerendert. |
| Fine | `2` | DrawingML-Effekte werden im Feinmodus gerendert, der eine erweiterte Verarbeitung erfordert. In diesem Modus liefert das Rendern von Effekten bessere Ergebnisse, allerdings zu einem höheren Leistungsaufwand alsSimplified mode. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
