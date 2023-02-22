---
title: VbaModuleCollection.Add
second_title: Aspose.Words för .NET API Referens
description: VbaModuleCollection metod. Lägger till en modul i samlingen.
type: docs
weight: 30
url: /sv/net/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection.Add method

Lägger till en modul i samlingen.

```csharp
public void Add(VbaModule vbaModule)
```

### Exempel

Visar hur man skapar ett VBA-projekt med hjälp av makron.

```csharp
Document doc = new Document();

// Skapa ett nytt VBA-projekt.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Skapa en ny modul och ange en makrokällkod.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Lägg till modulen i VBA-projektet.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### Se även

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* namnutrymme [Aspose.Words.Vba](../../vbamodulecollection/)
* hopsättning [Aspose.Words](../../../)


