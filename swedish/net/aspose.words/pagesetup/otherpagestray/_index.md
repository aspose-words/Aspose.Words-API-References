---
title: PageSetup.OtherPagesTray
linktitle: OtherPagesTray
articleTitle: OtherPagesTray
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PageSetup OtherPagesTray för att enkelt anpassa pappersfackinställningarna för din skrivare. Optimera utskriftseffektiviteten för varje avsnitt!
type: docs
weight: 300
url: /sv/net/aspose.words/pagesetup/otherpagestray/
---
## PageSetup.OtherPagesTray property

Hämtar eller ställer in vilket pappersfack (fack) som ska användas för alla utom den första sidan i ett avsnitt. Värdet är implementeringsspecifikt (skrivarspecifikt).

```csharp
public int OtherPagesTray { get; set; }
```

## Exempel

Visar hur man får alla avsnitt i ett dokument att använda standardpappersfacket för den valda skrivaren.

```csharp
Document doc = new Document();

// Hitta standardskrivaren som vi ska använda för att skriva ut det här dokumentet.
// Du kan definiera en specifik skrivare med hjälp av egenskapen "PrinterName" i PrinterSettings-objektet.
PrinterSettings settings = new PrinterSettings();

// Pappersfackets värde som lagras i dokument är skrivarspecifikt.
// Det här betyder att koden nedan återställer alla sidfackvärden för att använda skrivarens nuvarande standardfack.
// Du kan räkna upp PrinterSettings.PaperSources för att hitta de andra giltiga pappersfackvärdena för den valda skrivaren.
foreach (Section section in doc.Sections.OfType<Section>())
{
    section.PageSetup.FirstPageTray = settings.DefaultPageSettings.PaperSource.RawKind;
    section.PageSetup.OtherPagesTray = settings.DefaultPageSettings.PaperSource.RawKind;
}
```

Visar hur man konfigurerar utskrift med olika skrivarfack för olika pappersstorlekar.

```csharp
Document doc = new Document();

// Hitta standardskrivaren som vi ska använda för att skriva ut det här dokumentet.
// Du kan definiera en specifik skrivare med hjälp av egenskapen "PrinterName" i PrinterSettings-objektet.
PrinterSettings settings = new PrinterSettings();

// Det här är facket vi kommer att använda för sidor i pappersstorleken "A4".
int printerTrayForA4 = settings.PaperSources[0].RawKind;

// Det här är facket vi kommer att använda för sidor i pappersstorleken "Letter".
int printerTrayForLetter = settings.PaperSources[1].RawKind;

// Ändra PageSettings-objektet i det här avsnittet för att få Microsoft Word att instruera skrivaren
// att använda ett av facken vi identifierade ovan, beroende på pappersstorleken i det här avsnittet.
foreach (Section section in doc.Sections.OfType<Section>())
{
    if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.Letter)
    {
        section.PageSetup.FirstPageTray = printerTrayForLetter;
        section.PageSetup.OtherPagesTray = printerTrayForLetter;
    }
    else if (section.PageSetup.PaperSize == Aspose.Words.PaperSize.A4)
    {
        section.PageSetup.FirstPageTray = printerTrayForA4;
        section.PageSetup.OtherPagesTray = printerTrayForA4;
    }
}
```

### Se även

* class [PageSetup](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
