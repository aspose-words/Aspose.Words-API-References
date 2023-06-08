---
title: VbaModuleCollection.Add
linktitle: Add
articleTitle: Add
second_title: Aspose.Words for .NET
description: VbaModuleCollection Add method. Adds a module to the collection in C#.
type: docs
weight: 30
url: /net/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection.Add method

Adds a module to the collection.

```csharp
public void Add(VbaModule vbaModule)
```

## Examples

Shows how to create a VBA project using macros.

```csharp
Document doc = new Document();

// Create a new VBA project.
VbaProject project = new VbaProject();
project.Name = "Aspose.Project";
doc.VbaProject = project;

// Create a new module and specify a macro source code.
VbaModule module = new VbaModule();
module.Name = "Aspose.Module";
module.Type = VbaModuleType.ProceduralModule;
module.SourceCode = "New source code";

// Add the module to the VBA project.
doc.VbaProject.Modules.Add(module);

doc.Save(ArtifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### See Also

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* namespace [Aspose.Words.Vba](../../../aspose.words.vba/)
* assembly [Aspose.Words](../../../)
