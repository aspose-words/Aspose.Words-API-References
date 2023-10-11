---
title: Class PrinterSettingsContainer
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Rendering.PrinterSettingsContainer classe. Rappresenta una memoria per alcuni parametri diPrinterSettings oggetto.
type: docs
weight: 4580
url: /it/net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

Rappresenta una memoria per alcuni parametri diPrinterSettings oggetto.

Per saperne di più, visita il[Stampa di un documento a livello di codice o utilizzando le finestre di dialogo](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) articolo di documentazione.

```csharp
public class PrinterSettingsContainer
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(PrinterSettings) | Crea un contenitore perPrinterSettings . |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | VediPaperSource DiDefaultPageSettings . |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | VediPaperSizes . |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | VediPaperSources . |

### Osservazioni

Accesso ai dati diPrinterSettings richiede molto tempo. `PrinterSettingsContainer` memorizza nella cache i parametri daPrinterSettings , così la stampa funziona più velocemente.

### Esempi

Mostra come accedere ed elencare le origini e i formati carta della stampante.

```csharp
// Il "PrinterSettingsContainer" contiene un oggetto "PrinterSettings",
// che contiene dati univoci per diversi driver della stampante.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// La proprietà "PaperSizes" contiene l'elenco dei formati carta da utilizzare per la stampante.
// Sia PrinterSource che PrinterSize contengono una proprietà "RawKind",
// che equivale a un tipo di carta elencato nell'enumerazione PaperSourceKind.
// Se è presente un'origine carta con lo stesso valore "RawKind" di quello della pagina da stampare,
// la stampante stamperà la pagina utilizzando l'origine e il formato carta forniti.
// In caso contrario, la stampante utilizzerà per impostazione predefinita l'origine designata dalla proprietà "DefaultPageSettingsPaperSource".
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assemblea [Aspose.Words](../../)


