---
title: NumeralFormat Enum
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words för .NET
description: Aspose.Words.Saving.NumeralFormat uppräkning. Indikerar symboluppsättningen som används för att representera siffror vid återgivning till fasta sidformat i C#.
type: docs
weight: 5310
url: /sv/net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

Indikerar symboluppsättningen som används för att representera siffror vid återgivning till fasta sidformat.

```csharp
public enum NumeralFormat
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| European | `0` | Europeiska siffror: 0123456789. |
| ArabicIndic | `1` | Siffror som används på arabiska: ٠١٢٣٤٥٦٧٨٩. Unicode-intervall U+0660 - u+0669. |
| EasternArabicIndic | `2` | Siffror som används på persiska och urdu: ۰۱۲۳۴۵۶۷۸۹. Unicode-intervall U+06F0 - u+06F9. |
| Context | `3` | Symboluppsättningen bestäms utifrån kontext (lokal och RTL-egenskap). |
| System | `4` | DETTA ALTERNATIV STÖDS INTE. Symboluppsättningen bestäms från regionala inställningar. |

## Exempel

Visar hur du ställer in det sifferformat som används när du sparar till PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "NumeralFormat" till "NumeralFormat.ArabicIndic" till
// använd glyfer från intervallet U+0660 till U+0669 som siffror.
// Ställ in egenskapen "NumeralFormat" till "NumeralFormat.Context" till
// slå upp språket för att avgöra hur många glyfer som ska användas.
// Ställ in egenskapen "NumeralFormat" till "NumeralFormat.EasternArabicIndic" till
// använd glyfer från intervallet U+06F0 till U+06F9 som siffror.
// Ställ in egenskapen "NumeralFormat" till "NumeralFormat.European" för att använda europeiska siffror.
// Ställ in egenskapen "NumeralFormat" till "NumeralFormat.System" för att bestämma symboluppsättningen från regionala inställningar.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
