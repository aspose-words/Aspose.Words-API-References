---
title: PdfSaveOptions.DmlEffectsRenderingMode
linktitle: DmlEffectsRenderingMode
articleTitle: DmlEffectsRenderingMode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PdfSaveOptions DmlEffectsRenderingMode för att styra renderingen av DrawingML-effekter för förbättrad PDF-utdatakvalitet.
type: docs
weight: 100
url: /sv/net/aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/
---
## PdfSaveOptions.DmlEffectsRenderingMode property

Hämtar eller ställer in ett värde som avgör hur DrawingML-effekter renderas.

```csharp
public override DmlEffectsRenderingMode DmlEffectsRenderingMode { get; set; }
```

## Anmärkningar

Standardvärdet ärSimplified .

Den här egenskapen används när dokumentet exporteras till fasta sidformat.

Om[`Compliance`](../compliance/) är inställd påPdfA1a ellerPdfA1b , egenskapen returnerar alltidNone.

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

* enum [DmlEffectsRenderingMode](../../dmleffectsrenderingmode/)
* class [PdfSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
