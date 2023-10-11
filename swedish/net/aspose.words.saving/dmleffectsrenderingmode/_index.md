---
title: Enum DmlEffectsRenderingMode
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.DmlEffectsRenderingMode uppräkning. Anger hur DrawingMLeffekter renderas till fasta sidformat.
type: docs
weight: 4910
url: /sv/net/aspose.words.saving/dmleffectsrenderingmode/
---
## DmlEffectsRenderingMode enumeration

Anger hur DrawingML-effekter renderas till fasta sidformat.

```csharp
public enum DmlEffectsRenderingMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Simplified | `0` | Återgivning av DrawingML-effekter förenklas. |
| None | `1` | Inga DrawingML-effekter renderas. |
| Fine | `2` | DrawingML-effekter renderas i fint läge som involverar avancerad bearbetning. I detta läge ger rendering av effekter bättre resultat men till en högre prestandakostnad änSimplified läge. |

### Exempel

Visar hur du konfigurerar renderingskvaliteten för DrawingML-effekter i ett dokument när vi sparar det till PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape effects.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "DmlEffectsRenderingMode" till "DmlEffectsRenderingMode.None" för att ta bort alla DrawingML-effekter.
// Ställ in egenskapen "DmlEffectsRenderingMode" till "DmlEffectsRenderingMode.Simplified"
// för att rendera en förenklad version av DrawingML-effekter.
// Ställ in egenskapen "DmlEffectsRenderingMode" till "DmlEffectsRenderingMode.Fine" till
// gör DrawingML-effekter med mer precision och även med högre bearbetningskostnader.
options.DmlEffectsRenderingMode = effectsRenderingMode;

Assert.AreEqual(DmlRenderingMode.DrawingML, options.DmlRenderingMode);

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLEffects.pdf", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)


