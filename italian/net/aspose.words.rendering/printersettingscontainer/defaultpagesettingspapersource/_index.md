---
title: PrinterSettingsContainer.DefaultPageSettingsPaperSource
second_title: Aspose.Words per .NET API Reference
description: PrinterSettingsContainer proprietà. VediPaperSource diDefaultPageSettings .
type: docs
weight: 20
url: /it/net/aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/
---
## PrinterSettingsContainer.DefaultPageSettingsPaperSource property

VediPaperSource diDefaultPageSettings .

```csharp
public PaperSource DefaultPageSettingsPaperSource { get; }
```

### Esempi

Mostra come accedere ed elencare le origini e i formati carta della stampante.

```csharp
// Il "PrinterSettingsContainer" contiene un oggetto "PrinterSettings",
// che contiene dati univoci per diversi driver di stampa.
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
// Se è presente un'origine carta con lo stesso valore "RawKind" di quella della pagina da stampare,
// la stampante stamperà la pagina utilizzando l'origine carta e il formato forniti.
// In caso contrario, la stampante utilizzerà per impostazione predefinita l'origine designata dalla proprietà "DefaultPageSettingsPaperSource".
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### Guarda anche

* class [PrinterSettingsContainer](../)
* spazio dei nomi [Aspose.Words.Rendering](../../printersettingscontainer/)
* assemblea [Aspose.Words](../../../)


