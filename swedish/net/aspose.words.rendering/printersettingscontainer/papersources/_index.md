---
title: PrinterSettingsContainer.PaperSources
linktitle: PaperSources
articleTitle: PaperSources
second_title: Aspose.Words för .NET
description: Upptäck PrinterSettingsContainers PaperSources-egenskap för sömlös utskrift. Optimera dina utskriftsinställningar för bättre resultat och effektivitet!
type: docs
weight: 40
url: /sv/net/aspose.words.rendering/printersettingscontainer/papersources/
---
## PrinterSettingsContainer.PaperSources property

SePaperSources .

```csharp
public PaperSourceCollection PaperSources { get; }
```

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

* class [PrinterSettingsContainer](../)
* namnutrymme [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* hopsättning [Aspose.Words](../../../)
