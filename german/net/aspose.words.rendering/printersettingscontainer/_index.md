---
title: PrinterSettingsContainer Class
linktitle: PrinterSettingsContainer
articleTitle: PrinterSettingsContainer
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Rendering.PrinterSettingsContainer für die effiziente Verwaltung von PrinterSettings-Parametern und verbessern Sie so Ihr Dokument-Rendering-Erlebnis.
type: docs
weight: 5310
url: /de/net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

Stellt einen Speicher für einige Parameter dar vonPrinterSettings Objekt.

Um mehr zu erfahren, besuchen Sie die[Drucken eines Dokuments programmgesteuert oder mithilfe von Dialogen](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) Dokumentationsartikel.

```csharp
public class PrinterSettingsContainer
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(*PrinterSettings*) | Erstellt einen Container fürPrinterSettings . |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | SiehePaperSource vonDefaultPageSettings . |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | SiehePaperSizes . |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | SiehePaperSources . |

## Bemerkungen

Zugriff auf Daten vonPrinterSettings dauert lange. `PrinterSettingsContainer` speichert Parameter ausPrinterSettings , damit das Drucken schneller geht.

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

* namensraum [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Montage [Aspose.Words](../../)
