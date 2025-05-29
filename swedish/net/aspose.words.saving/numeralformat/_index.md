---
title: NumeralFormat Enum
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.NumeralFormat enum för optimal talrepresentation i fasta sidformat. Förbättra din dokumentrendering idag!
type: docs
weight: 6090
url: /sv/net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

Anger symboluppsättningen som används för att representera tal vid rendering till fasta sidformat.

```csharp
public enum NumeralFormat
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| European | `0` | Europeiska siffror: 0123456789. |
| ArabicIndic | `1` | Siffror som används på arabiska: ٠١٢٣٤٥٦٧٨٩. Unicode-intervall U+0660 - u+0669. |
| EasternArabicIndic | `2` | Siffror som används på persiska och urdu: 0123456789. Unicode-intervall U+06F0 - u+06F9. |
| Context | `3` | Symboluppsättningen bestäms utifrån kontext (språk och RTL-egenskap). |
| System | `4` | DETTA ALTERNATIV STÖDS INTE. Symboluppsättningen bestäms utifrån regionala inställningar. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
