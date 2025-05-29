---
title: MultiplePagesType Enum
linktitle: MultiplePagesType
articleTitle: MultiplePagesType
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Settings.MultiplePagesType-enum för effektiva dokumentutskriftsalternativ. Optimera ditt arbetsflöde med flexibla utskriftsinställningar!
type: docs
weight: 6700
url: /sv/net/aspose.words.settings/multiplepagestype/
---
## MultiplePagesType enumeration

Anger hur dokumentet skrivs ut.

```csharp
public enum MultiplePagesType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Normal | `0` | Normal utskrift, inga angivna sidor. |
| MirrorMargins | `1` | Byter vänster- och högermarginaler på motstående sidor. |
| TwoPagesPerSheet | `2` | Skriver ut två sidor per ark. |
| BookFoldPrinting | `3` | Anger om dokumentet ska skrivas ut som en bokvikning. |
| BookFoldPrintingReverse | `4` | Anger om dokumentet ska skrivas ut som en omvänd bokvikning. |
| Default | `0` | Standardvärdet ärNormal |

## Exempel

Visar hur man konfigurerar ett dokument som kan skrivas ut som en bokvikning.

```csharp
Document doc = new Document();

// Infoga text som sträcker sig över 16 sidor.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("My Booklet:");

for (int i = 0; i < 15; i++)
{
    builder.InsertBreak(BreakType.PageBreak);
    builder.Write($"Booklet face #{i}");
}

// Konfigurera den första sektionens "PageSetup"-egenskap för att skriva ut dokumentet i form av en bokvikning.
// När vi skriver ut detta dokument på båda sidor kan vi ta sidorna och stapla dem
// och vik dem alla på mitten samtidigt. Innehållet i dokumentet kommer att radas upp till en bokvikning.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;

// Vi kan bara ange antalet ark i multiplar av 4.
pageSetup.SheetsPerBooklet = 4;

doc.Save(ArtifactsDir + "PageSetup.Booklet.docx");
```

### Se även

* namnutrymme [Aspose.Words.Settings](../../aspose.words.settings/)
* hopsättning [Aspose.Words](../../)
