---
title: FixedPageSaveOptions.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words för .NET
description: FixedPageSaveOptions ColorMode fast egendom. Hämtar eller ställer in ett värde som bestämmer hur färger återges i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

Hämtar eller ställer in ett värde som bestämmer hur färger återges.

```csharp
public ColorMode ColorMode { get; set; }
```

## Anmärkningar

Standardvärdet ärNormal .

## Exempel

Visar hur du ändrar bildfärg med egenskapen sparalternativ.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
// Ställ in egenskapen "ColorMode" till "Gråskala" för att återge alla bilder från dokumentet i svartvitt.
// Storleken på utdatadokumentet kan vara större med den här inställningen.
// Ställ in egenskapen "ColorMode" till "Normal" för att återge alla bilder i färg.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Se även

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
