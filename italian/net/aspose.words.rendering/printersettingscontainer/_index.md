---
title: PrinterSettingsContainer Class
linktitle: PrinterSettingsContainer
articleTitle: PrinterSettingsContainer
second_title: Aspose.Words per .NET
description: Esplora la classe Aspose.Words.Rendering.PrinterSettingsContainer per una gestione efficiente dei parametri PrinterSettings, migliorando l'esperienza di rendering dei documenti.
type: docs
weight: 5310
url: /it/net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

Rappresenta un archivio per alcuni parametri diPrinterSettings oggetto.

Per saperne di più, visita il[Stampa di un documento tramite programmazione o tramite finestre di dialogo](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) articolo di documentazione.

```csharp
public class PrinterSettingsContainer
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(*PrinterSettings*) | Crea un contenitore perPrinterSettings . |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | VediPaperSource DiDefaultPageSettings . |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | VediPaperSizes . |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | VediPaperSources . |

## Osservazioni

Accesso ai dati diPrinterSettings ci vuole molto tempo. `PrinterSettingsContainer` memorizza nella cache i parametri daPrinterSettings , quindi la stampa funziona più velocemente.

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

* spazio dei nomi [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../)
