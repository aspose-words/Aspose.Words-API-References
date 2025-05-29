---
title: VbaModuleCollection Class
linktitle: VbaModuleCollection
articleTitle: VbaModuleCollection
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Vba.VbaModuleCollection, ditt viktiga verktyg för att effektivt hantera VbaModule-objekt i dokumentautomation.
type: docs
weight: 7410
url: /sv/net/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class

Representerar en samling av[`VbaModule`](../vbamodule/) objekt.

För att lära dig mer, besök[Arbeta med VBA-makron](https://docs.aspose.com/words/net/working-with-vba-macros/) dokumentationsartikel.

```csharp
public sealed class VbaModuleCollection : IEnumerable<VbaModule>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.vba/vbamodulecollection/count/) { get; } | Returnerar antalet VBA-moduler i samlingen. |
| [Item](../../aspose.words.vba/vbamodulecollection/item/) { get; } | Hämtar en[`VbaModule`](../vbamodule/) objekt av index. (2 indexers) |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.vba/vbamodulecollection/add/)(*[VbaModule](../vbamodule/)*) | Lägger till en modul i samlingen. |
| [Remove](../../aspose.words.vba/vbamodulecollection/remove/)(*[VbaModule](../vbamodule/)*) | Tar bort den angivna modulen från samlingen. |

## Exempel

Visar hur man kommer åt ett dokuments VBA-projektinformation.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Ett VBA-projekt innehåller en samling VBA-moduler.
VbaProject vbaProject = doc.VbaProject;
Console.WriteLine(vbaProject.IsSigned
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules;

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Ange ny källkod för VBA-modulen. Du kan komma åt VBA-moduler i samlingen antingen via index eller namn.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Ta bort en modul från samlingen.
vbaModules.Remove(vbaModules[2]);
```

### Se även

* class [VbaModule](../vbamodule/)
* namnutrymme [Aspose.Words.Vba](../../aspose.words.vba/)
* hopsättning [Aspose.Words](../../)
