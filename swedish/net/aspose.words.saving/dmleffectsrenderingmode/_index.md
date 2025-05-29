---
title: DmlEffectsRenderingMode Enum
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words DmlEffectsRenderingMode-enum för optimerad DrawingML-effektrendering i fasta sidformat. Förbättra din dokumentkvalitet!
type: docs
weight: 5660
url: /sv/net/aspose.words.saving/dmleffectsrenderingmode/
---
## DmlEffectsRenderingMode enumeration

Anger hur DrawingML-effekter återges till fasta sidformat.

```csharp
public enum DmlEffectsRenderingMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Simplified | `0` | Rendering av DrawingML-effekter är förenklad. |
| None | `1` | Inga DrawingML-effekter renderas. |
| Fine | `2` | DrawingML-effekter renderas i finläge vilket innebär avancerad bearbetning. I det här läget ger rendering av effekter bättre resultat men till en högre prestandakostnad änSimplified läge. |

## Exempel

Visar hur man konfigurerar renderingskvaliteten för DrawingML-effekter i ett dokument när vi sparar det som PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "DmlEffectsRenderingMode" till "DmlEffectsRenderingMode.None" för att ignorera alla DrawingML-effekter.
// Ställ in egenskapen "DmlEffectsRenderingMode" till "DmlEffectsRenderingMode.Simplified"
// för att rendera en förenklad version av DrawingML-effekter.
// Ställ in egenskapen "DmlEffectsRenderingMode" till "DmlEffectsRenderingMode.Fine" för att
// rendera DrawingML-effekter med större noggrannhet och även med högre bearbetningskostnad.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
