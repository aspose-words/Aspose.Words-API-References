---
title: PrinterSettingsContainer Class
linktitle: PrinterSettingsContainer
articleTitle: PrinterSettingsContainer
second_title: Aspose.Words for .NET
description: Aspose.Words.Rendering.PrinterSettingsContainer class. Represent a storage for some parameters of PrinterSettings object in C#.
type: docs
weight: 4560
url: /net/aspose.words.rendering/printersettingscontainer/
---
## PrinterSettingsContainer class

Represent a storage for some parameters of PrinterSettings object.

To learn more, visit the [Printing a Document Programmatically or Using Dialogs](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) documentation article.

```csharp
public class PrinterSettingsContainer
```

## Constructors

| Name | Description |
| --- | --- |
| [PrinterSettingsContainer](printersettingscontainer/)(*PrinterSettings*) | Creates a container for PrinterSettings. |

## Properties

| Name | Description |
| --- | --- |
| [DefaultPageSettingsPaperSource](../../aspose.words.rendering/printersettingscontainer/defaultpagesettingspapersource/) { get; } | See PaperSource of DefaultPageSettings. |
| [PaperSizes](../../aspose.words.rendering/printersettingscontainer/papersizes/) { get; } | See PaperSizes. |
| [PaperSources](../../aspose.words.rendering/printersettingscontainer/papersources/) { get; } | See PaperSources. |

## Remarks

Access to data of PrinterSettings takes long time. `PrinterSettingsContainer` caches parameters from PrinterSettings, so printing works faster.

## Examples

Shows how to access and list your printer's paper sources and sizes.

```csharp
// The "PrinterSettingsContainer" contains a "PrinterSettings" object,
// which contains unique data for different printer drivers.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// The "PaperSizes" property contains the list of paper sizes to instruct the printer to use.
// Both the PrinterSource and PrinterSize contain a "RawKind" property,
// which equates to a paper type listed on the PaperSourceKind enum.
// If there is a paper source with the same "RawKind" value as that of the printing page,
// the printer will print the page using the provided paper source and size.
// Otherwise, the printer will default to the source designated by the "DefaultPageSettingsPaperSource" property.
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### See Also

* namespace [Aspose.Words.Rendering](../../aspose.words.rendering/)
* assembly [Aspose.Words](../../)
