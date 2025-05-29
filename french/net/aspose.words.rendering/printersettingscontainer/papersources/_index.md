---
title: PrinterSettingsContainer.PaperSources
linktitle: PaperSources
articleTitle: PaperSources
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PaperSources de PrinterSettingsContainer pour une impression fluide. Optimisez vos paramètres d'impression pour de meilleurs résultats et une meilleure efficacité !
type: docs
weight: 40
url: /fr/net/aspose.words.rendering/printersettingscontainer/papersources/
---
## PrinterSettingsContainer.PaperSources property

VoirPaperSources .

```csharp
public PaperSourceCollection PaperSources { get; }
```

## Exemples

Montre comment accéder et répertorier les sources et les formats de papier de votre imprimante.

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

// La propriété « PaperSizes » contient la liste des formats de papier à utiliser par l'imprimante.
// PrinterSource et PrinterSize contiennent tous deux une propriété « RawKind »,
// qui équivaut à un type de papier répertorié dans l'énumération PaperSourceKind.
// S'il existe une source de papier avec la même valeur « RawKind » que celle de la page d'impression,
// l'imprimante imprimera la page en utilisant la source de papier et le format fournis.
// Sinon, l'imprimante utilisera par défaut la source désignée par la propriété « DefaultPageSettingsPaperSource ».
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
