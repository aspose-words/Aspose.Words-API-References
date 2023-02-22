---
title: PageSetup.FirstPageTray
second_title: Aspose.Words för .NET API Referens
description: PageSetup fast egendom. Hämtar eller ställer in pappersfacket fack som ska användas för den första sidan i ett avsnitt. Värdet är implementeringsspecifikt skrivaren.
type: docs
weight: 130
url: /sv/net/aspose.words/pagesetup/firstpagetray/
---
## PageSetup.FirstPageTray property

Hämtar eller ställer in pappersfacket (fack) som ska användas för den första sidan i ett avsnitt. Värdet är implementeringsspecifikt (skrivaren).

```csharp
public int FirstPageTray { get; set; }
```

### Exempel

Visar hur du får alla avsnitt i ett dokument att använda standardpappersfacket för den valda skrivaren.

```csharp
Document doc = new Document();

// Hitta standardskrivaren som vi kommer att använda för att skriva ut detta dokument.
// Du kan definiera en specifik skrivare med "PrinterName"-egenskapen för objektet PrinterSettings.
PrinterSettings settings = new PrinterSettings();

// Pappersfackvärdet som lagras i dokument är skrivarspecifikt.
// Detta betyder att koden nedan återställer alla sidfackvärden för att använda skrivarens nuvarande standardfack.
// Du kan räkna upp PrinterSettings.PaperSources för att hitta andra giltiga pappersfackvärden för den valda skrivaren.
foreach (Section section in doc.Sections.OfType<Section>())
{
    section.PageSetup.FirstPageTray = settings.DefaultPageSettings.PaperSource.RawKind;
    section.PageSetup.OtherPagesTray = settings.DefaultPageSettings.PaperSource.RawKind;
}
```

Visar hur du ställer in utskrift med olika skrivarfack för olika pappersstorlekar.

```csharp
Document doc = new Document();

// Hitta standardskrivaren som vi kommer att använda för att skriva ut detta dokument.
// Du kan definiera en specifik skrivare med "PrinterName"-egenskapen för objektet PrinterSettings.
PrinterSettings settings = new PrinterSettings();

// Det här är facket vi kommer att använda för sidor i pappersstorleken "A4".
int printerTrayForA4 = settings.PaperSources[0].RawKind;

// Det här är facket vi kommer att använda för sidor i pappersstorleken "Letter".
int printerTrayForLetter = settings.PaperSources[1].RawKind;

// Ändra objektet PageSettings i det här avsnittet för att få Microsoft Word att instruera skrivaren
// för att använda ett av magasinen vi identifierade ovan, beroende på det här avsnittets pappersstorlek.
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
* namnutrymme [Aspose.Words](../../pagesetup/)
* hopsättning [Aspose.Words](../../../)


