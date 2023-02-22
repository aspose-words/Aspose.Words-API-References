---
title: Class VbaModule
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Vba.VbaModule klass. Ger tillgång till VBAprojektmodul.
type: docs
weight: 6240
url: /sv/net/aspose.words.vba/vbamodule/
---
## VbaModule class

Ger tillgång till VBA-projektmodul.

```csharp
public class VbaModule
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [VbaModule](vbamodule/)() | Skapar en tom modul. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Name](../../aspose.words.vba/vbamodule/name/) { get; set; } | Hämtar eller ställer in VBA-projektmodulens namn. |
| [SourceCode](../../aspose.words.vba/vbamodule/sourcecode/) { get; set; } | Hämtar eller ställer in VBA-projektmodulens källkod. |
| [Type](../../aspose.words.vba/vbamodule/type/) { get; set; } | Anger om modulen är en procedurmodul, dokumentmodul, klassmodul eller designermodul. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clone](../../aspose.words.vba/vbamodule/clone/)() | Utför en kopia av`VbaModule` . |

### Exempel

Visar hur man kommer åt ett dokuments VBA-projektinformation.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// Ett VBA-projekt innehåller en samling VBA-moduler.
VbaProject vbaProject = doc.VbaProject;
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Ställ in ny källkod för VBA-modulen. Du kan komma åt VBA-moduler i samlingen antingen med index eller namn.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Ta bort en modul från samlingen.
vbaModules.Remove(vbaModules[2]);
```

### Se även

* namnutrymme [Aspose.Words.Vba](../../aspose.words.vba/)
* hopsättning [Aspose.Words](../../)


