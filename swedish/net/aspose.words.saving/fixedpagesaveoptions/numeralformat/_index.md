---
title: FixedPageSaveOptions.NumeralFormat
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen NumeralFormat i FixedPageSaveOptions för att anpassa numerisk rendering. Växla enkelt till europeiska siffror för förbättrad dokumentpresentation.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

Hämtar eller sätter[`NumeralFormat`](../../numeralformat/) används för rendering av siffror. Europeiska siffror används som standard.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

## Anmärkningar

Om värdet på den här egenskapen ändras och sidlayouten redan är skapad så [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) anropas automatiskt för att uppdatera eventuella ändringar.

## Exempel

Visar hur man ställer in sifferformatet som används när man sparar till PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "NumeralFormat" till "NumeralFormat.ArabicIndic" för att
// använd tecken från intervallet U+0660 till U+0669 som tal.
// Sätt egenskapen "NumeralFormat" till "NumeralFormat.Context" för att
// slå upp språkinställningen för att avgöra hur många tecken som ska användas.
// Ställ in egenskapen "NumeralFormat" till "NumeralFormat.EasternArabicIndic" för att
// använd tecken från U+06F0 till U+06F9-intervallet som tal.
// Sätt egenskapen "NumeralFormat" till "NumeralFormat.European" för att använda europeiska siffror.
// Sätt egenskapen "NumeralFormat" till "NumeralFormat.System" för att bestämma symboluppsättningen från regionala inställningar.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Se även

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
