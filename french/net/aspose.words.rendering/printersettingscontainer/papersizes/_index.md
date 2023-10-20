---
title: PrinterSettingsContainer.PaperSizes
linktitle: PaperSizes
articleTitle: PaperSizes
second_title: Aspose.Words pour .NET
description: PrinterSettingsContainer PaperSizes propriété. VoirPaperSizes  en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.rendering/printersettingscontainer/papersizes/
---
## PrinterSettingsContainer.PaperSizes property

VoirPaperSizes .

```csharp
public PaperSizeCollection PaperSizes { get; }
```

## Exemples

Montre comment accéder et répertorier les sources et formats de papier de votre imprimante.

```csharp
// Le "PrinterSettingsContainer" contient un objet "PrinterSettings",
// qui contient des données uniques pour différents pilotes d'imprimante.
PrinterSettingsContainer container = new PrinterSettingsContainer(new PrinterSettings());

Console.WriteLine($"This printer contains {container.PaperSources.Count} printer paper sources:");
foreach (PaperSource paperSource in container.PaperSources)
{
    bool isDefault = container.DefaultPageSettingsPaperSource.SourceName == paperSource.SourceName;
    Console.WriteLine($"\t{paperSource.SourceName}, " +
                      $"RawKind: {paperSource.RawKind} {(isDefault ? "(Default)" : "")}");
}

// La propriété "PaperSizes" contient la liste des formats de papier à demander à l'imprimante.
// PrinterSource et PrinterSize contiennent tous deux une propriété "RawKind",
// ce qui équivaut à un type de papier répertorié dans l'énumération PaperSourceKind.
// S'il existe une source papier avec la même valeur "RawKind" que celle de la page à imprimer,
// l'imprimante imprimera la page en utilisant la source et le format de papier fournis.
// Sinon, l'imprimante utilisera par défaut la source désignée par la propriété "DefaultPageSettingsPaperSource".
Console.WriteLine($"{container.PaperSizes.Count} paper sizes:");
foreach (System.Drawing.Printing.PaperSize paperSize in container.PaperSizes)
{
    Console.WriteLine($"\t{paperSize}, RawKind: {paperSize.RawKind}");
}
```

### Voir également

* class [PrinterSettingsContainer](../)
* espace de noms [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Assemblée [Aspose.Words](../../../)
