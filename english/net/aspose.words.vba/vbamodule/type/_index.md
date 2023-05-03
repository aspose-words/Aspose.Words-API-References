---
title: VbaModule.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET API Reference
description: VbaModule Type property. Specifies whether the module is a procedural module document module class module or designer module in C#.
type: docs
weight: 40
url: /net/aspose.words.vba/vbamodule/type/
---
## VbaModule.Type property

Specifies whether the module is a procedural module, document module, class module, or designer module.

```csharp
public VbaModuleType Type { get; set; }
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

* enum [VbaModuleType](../../vbamoduletype/)
* class [VbaModule](../)
* namespace [Aspose.Words.Vba](../../vbamodule/)
* assembly [Aspose.Words](../../../)
