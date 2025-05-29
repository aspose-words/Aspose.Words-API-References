---
title: PrinterSettingsContainer.PaperSources
linktitle: PaperSources
articleTitle: PaperSources
second_title: Aspose.Words für .NET
description: Entdecken Sie die PaperSources-Eigenschaft des PrinterSettingsContainers für nahtloses Drucken. Optimieren Sie Ihre Druckeinstellungen für bessere Ergebnisse und mehr Effizienz!
type: docs
weight: 40
url: /de/net/aspose.words.rendering/printersettingscontainer/papersources/
---
## PrinterSettingsContainer.PaperSources property

SiehePaperSources .

```csharp
public PaperSourceCollection PaperSources { get; }
```

## Beispiele

Zeigt, wie Sie auf die Papierquellen und -formate Ihres Druckers zugreifen und diese auflisten.

```csharp
// Der "PrinterSettingsContainer" enthält ein "PrinterSettings"-Objekt,
// die eindeutige Daten für verschiedene Druckertreiber enthält.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// Die Eigenschaft „PaperSizes“ enthält die Liste der Papiergrößen, die der Drucker verwenden soll.
// Sowohl PrinterSource als auch PrinterSize enthalten eine "RawKind"-Eigenschaft,
// was einem Papiertyp entspricht, der in der Aufzählung PaperSourceKind aufgeführt ist.
// Wenn es eine Papierquelle mit dem gleichen „RawKind“-Wert wie die Druckseite gibt,
// Der Drucker druckt die Seite mit der angegebenen Papierquelle und -größe.
// Andernfalls verwendet der Drucker standardmäßig die Quelle, die durch die Eigenschaft „DefaultPageSettingsPaperSource“ angegeben ist.
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### Siehe auch

* class [PrinterSettingsContainer](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)
