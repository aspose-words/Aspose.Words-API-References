---
title: PrinterSettingsContainer
linktitle: PrinterSettingsContainer
articleTitle: PrinterSettingsContainer
second_title: Aspose.Words for .NET
description: Discover the PrinterSettingsContainer constructor, efficiently create and manage your printer settings with ease. Optimize your printing experience today!
type: docs
weight: 10
url: /net/aspose.words.rendering/printersettingscontainer/printersettingscontainer/
---
## PrinterSettingsContainer constructor

Creates a container for PrinterSettings.

```csharp
public PrinterSettingsContainer(PrinterSettings settings)
```

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

* class [PrinterSettingsContainer](../)
* namespace [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* assembly [Aspose.Words](../../../)
