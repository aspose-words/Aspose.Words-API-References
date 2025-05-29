---
title: DmlRenderingMode Enum
linktitle: DmlRenderingMode
articleTitle: DmlRenderingMode
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words.Saving.DmlRenderingMode förbättrar DrawingML-formrendering för högkvalitativa fasta sidformat. Optimera dina dokumentgrafik!
type: docs
weight: 5670
url: /sv/net/aspose.words.saving/dmlrenderingmode/
---
## DmlRenderingMode enumeration

Anger hur DrawingML-former återges till fasta sidformat.

```csharp
public enum DmlRenderingMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Fallback | `0` | Om en reservform är tillgänglig för DrawingML, renderar Aspose.Words reservformen istället för DrawingML. |
| DrawingML | `1` | Aspose.Words ignorerar DrawingMLs reservform och renderar DrawingML självt. Detta är standardläget. |

## Exempel

Visar hur man renderar reservformer när man sparar till PDF.

```csharp
Document doc = new Document(MyDir + "DrawingML shape fallbacks.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "DmlRenderingMode" till "DmlRenderingMode.Fallback"
// för att ersätta DML-former med deras reservformer.
// Ställ in egenskapen "DmlRenderingMode" till "DmlRenderingMode.DrawingML"
// för att rendera själva DML-formerna.
options.DmlRenderingMode = dmlRenderingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.DrawingMLFallback.pdf", options);
```

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
