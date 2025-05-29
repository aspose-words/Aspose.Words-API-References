---
title: VbaProject
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words för .NET
description: Skapa enkelt ett nytt Vba-projekt med vårt konstruktörsverktyg. Börja din programmeringsresa med ett tomt projekt och släpp lös din kreativitet!
type: docs
weight: 10
url: /sv/net/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject constructor

Skapar ett tomrum[`VbaProject`](../) .

```csharp
public VbaProject()
```

## Exempel

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

* class [VbaProject](../)
* namnutrymme [Aspose.Words.Vba](../../../aspose.words.vba/)
* hopsättning [Aspose.Words](../../../)
