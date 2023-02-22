---
title: VbaProject.Modules
second_title: Aspose.Words för .NET API Referens
description: VbaProject fast egendom. Returnerar samling av VBAprojektmoduler.
type: docs
weight: 40
url: /sv/net/aspose.words.vba/vbaproject/modules/
---
## VbaProject.Modules property

Returnerar samling av VBA-projektmoduler.

```csharp
public VbaModuleCollection Modules { get; }
```

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

* class [VbaModuleCollection](../../vbamodulecollection/)
* class [VbaProject](../)
* namnutrymme [Aspose.Words.Vba](../../vbaproject/)
* hopsättning [Aspose.Words](../../../)


