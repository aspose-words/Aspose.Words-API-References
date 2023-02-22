---
title: VbaModuleCollection.Item
second_title: Aspose.Words för .NET API Referens
description: VbaModuleCollection fast egendom. Hämtar enVbaModule objekt efter index.
type: docs
weight: 20
url: /sv/net/aspose.words.vba/vbamodulecollection/item/
---
## VbaModuleCollection indexer (1 of 2)

Hämtar en[`VbaModule`](../../vbamodule/) objekt efter index.

```csharp
public VbaModule this[int index] { get; }
```

| Parameter | Beskrivning |
| --- | --- |
| index | Nollbaserat index för modulen att hämta. |

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* namnutrymme [Aspose.Words.Vba](../../vbamodulecollection/)
* hopsättning [Aspose.Words](../../../)

---

## VbaModuleCollection indexer (2 of 2)

Hämtar en[`VbaModule`](../../vbamodule/)objekt med namn, eller noll om det inte hittas.

```csharp
public VbaModule this[string name] { get; }
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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* namnutrymme [Aspose.Words.Vba](../../vbamodulecollection/)
* hopsättning [Aspose.Words](../../../)


