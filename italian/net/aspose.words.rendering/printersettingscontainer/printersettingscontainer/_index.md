---
title: PrinterSettingsContainer
linktitle: PrinterSettingsContainer
articleTitle: PrinterSettingsContainer
second_title: Aspose.Words per .NET
description: Scopri il costruttore PrinterSettingsContainer, crea e gestisci in modo efficiente le impostazioni della tua stampante con facilità. Ottimizza la tua esperienza di stampa oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words.rendering/printersettingscontainer/printersettingscontainer/
---
## PrinterSettingsContainer constructor

Crea un contenitore perPrinterSettings .

```csharp
public PrinterSettingsContainer(PrinterSettings settings)
```

## Esempi

Mostra come accedere ed elencare le fonti e i formati della carta della stampante.

```csharp
// "PrinterSettingsContainer" contiene un oggetto "PrinterSettings",
// che contiene dati univoci per diversi driver di stampante.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// La proprietà "PaperSizes" contiene l'elenco dei formati di carta da utilizzare per la stampante.
// Sia PrinterSource che PrinterSize contengono una proprietà "RawKind",
// che equivale a un tipo di carta elencato nell'enum PaperSourceKind.
// Se è presente un'origine carta con lo stesso valore "RawKind" della pagina da stampare,
// la stampante stamperà la pagina utilizzando l'alimentazione e il formato carta specificati.
// In caso contrario, la stampante utilizzerà per impostazione predefinita la sorgente designata dalla proprietà "DefaultPageSettingsPaperSource".
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### Guarda anche

* class [PrinterSettingsContainer](../)
* spazio dei nomi [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../../)
