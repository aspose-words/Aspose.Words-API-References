---
title: VbaProject.IsSigned
linktitle: IsSigned
articleTitle: IsSigned
second_title: Aspose.Words för .NET
description: Upptäck egenskapen VbaProject IsSigned för att enkelt verifiera projektsignaturer och förbättra din kodsäkerhet. Se till att dina VBA-projekt är betrodda!
type: docs
weight: 40
url: /sv/net/aspose.words.vba/vbaproject/issigned/
---
## VbaProject.IsSigned property

Visar om[`VbaProject`](../) är signerad eller inte.

```csharp
public bool IsSigned { get; }
```

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

* class [VbaProject](../)
* namnutrymme [Aspose.Words.Vba](../../../aspose.words.vba/)
* hopsättning [Aspose.Words](../../../)
