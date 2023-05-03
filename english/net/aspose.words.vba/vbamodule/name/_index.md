---
title: VbaModule.Name
linktitle: Name
second_title: Aspose.Words for .NET API Reference
description: VbaModule Name property. Gets or sets VBA project module name in C#.
type: docs
weight: 20
url: /net/aspose.words.vba/vbamodule/name/
---
## VbaModule.Name property

Gets or sets VBA project module name.

```csharp
public string Name { get; set; }
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

Shows how to access a document's VBA project information.

```csharp
Document doc = new Document(MyDir + "VBA project.docm");

// A VBA project contains a collection of VBA modules.
VbaProject vbaProject = doc.VbaProject;
Console.WriteLine(vbaProject.IsSigned
    ? $"Project name: {vbaProject.Name} signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n"
    : $"Project name: {vbaProject.Name} not signed; Project code page: {vbaProject.CodePage}; Modules count: {vbaProject.Modules.Count()}\n");

VbaModuleCollection vbaModules = doc.VbaProject.Modules; 

Assert.AreEqual(vbaModules.Count(), 3);

foreach (VbaModule module in vbaModules)
    Console.WriteLine($"Module name: {module.Name};\nModule code:\n{module.SourceCode}\n");

// Set new source code for VBA module. You can access VBA modules in the collection either by index or by name.
vbaModules[0].SourceCode = "Your VBA code...";
vbaModules["Module1"].SourceCode = "Your VBA code...";

// Remove a module from the collection.
vbaModules.Remove(vbaModules[2]);
```

### See Also

* class [VbaModule](../)
* namespace [Aspose.Words.Vba](../../vbamodule/)
* assembly [Aspose.Words](../../../)
