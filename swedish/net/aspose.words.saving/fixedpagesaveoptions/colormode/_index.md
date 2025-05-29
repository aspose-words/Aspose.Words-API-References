---
title: FixedPageSaveOptions.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FixedPageSaveOptions ColorMode för att anpassa färgåtergivningen för förbättrad dokumentkvalitet och visuell attraktionskraft. Optimera din utskrift idag!
type: docs
weight: 10
url: /sv/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

Hämtar eller ställer in ett värde som avgör hur färger återges.

```csharp
public ColorMode ColorMode { get; set; }
```

## Anmärkningar

Standardvärdet ärNormal .

## Exempel

Visar hur man ändrar bildfärg med egenskapen för att spara alternativ.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
// Ställ in egenskapen "ColorMode" till "Grayscale" för att rendera alla bilder från dokumentet i svartvitt.
// Storleken på utdatadokumentet kan vara större med den här inställningen.
// Ställ in egenskapen "ColorMode" till "Normal" för att rendera alla bilder i färg.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Se även

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
