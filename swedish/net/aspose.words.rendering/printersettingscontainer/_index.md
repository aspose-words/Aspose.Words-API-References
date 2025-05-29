---
title: PrinterSettingsContainer Class
linktitle: PrinterSettingsContainer
articleTitle: PrinterSettingsContainer
second_title: Aspose.Words för .NET
description: Utforska klassen Aspose.Words.Rendering.PrinterSettingsContainer för effektiv hantering av PrinterSettings-parametrar, vilket förbättrar din dokumentrenderingsupplevelse.
type: docs
weight: 5310
url: /sv/net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

Representerar ett minne för vissa parametrar avPrinterSettings objekt.

För att lära dig mer, besök[Skriva ut ett dokument programmatiskt eller med hjälp av dialogrutor](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) dokumentationsartikel.

```csharp
public class PrinterSettingsContainer
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(*PrinterSettings*) | Skapar en behållare förPrinterSettings . |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | SePaperSource avDefaultPageSettings . |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | SePaperSizes . |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | SePaperSources . |

## Anmärkningar

Åtkomst till data förPrinterSettings tar lång tid. `PrinterSettingsContainer` cachar parametrar frånPrinterSettings , så att utskriften fungerar snabbare.

## Exempel

Visar hur du får åtkomst till och listar skrivarens papperskällor och storlekar.

```csharp
// "PrinterSettingsContainer" innehåller ett "PrinterSettings"-objekt,
// som innehåller unika data för olika skrivardrivrutiner.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// Egenskapen "PaperSizes" innehåller en lista över pappersstorlekar som skrivaren ska använda.
// Både PrinterSource och PrinterSize innehåller en "RawKind"-egenskap,
// vilket motsvarar en papperstyp som listas i PaperSourceKind-uppräkningen.
// Om det finns en papperskälla med samma "RawKind"-värde som utskriftssidan,
// skrivaren skriver ut sidan med den angivna papperskällan och storleken.
// Annars kommer skrivaren att använda den källa som anges av egenskapen "DefaultPageSettingsPaperSource" som standard.
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### Se även

* namnutrymme [Aspose.Words.Rendering](../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../)
