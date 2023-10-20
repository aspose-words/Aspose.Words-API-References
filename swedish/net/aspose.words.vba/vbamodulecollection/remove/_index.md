---
title: VbaModuleCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words för .NET
description: VbaModuleCollection Remove metod. Tar bort den angivna modulen från samlingen i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.vba/vbamodulecollection/remove/
---
## VbaModuleCollection.Remove method

Tar bort den angivna modulen från samlingen.

```csharp
public void Remove(VbaModule module)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| module | VbaModule | Modulen att ta bort. |

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

// Ställ in ny källkod för VBA-modulen. Du kan komma åt VBA-moduler i samlingen antingen med index eller namn.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Ta bort en modul från samlingen.
vbaModules.Remove(vbaModules[2]);
```

### Se även

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* namnutrymme [Aspose.Words.Vba](../../../aspose.words.vba/)
* hopsättning [Aspose.Words](../../../)
