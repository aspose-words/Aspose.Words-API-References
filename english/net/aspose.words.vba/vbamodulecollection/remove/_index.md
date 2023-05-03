---
title: VbaModuleCollection.Remove
linktitle: Remove
second_title: Aspose.Words for .NET API Reference
description: VbaModuleCollection Remove method. Removes the specified module from the collection in C#.
type: docs
weight: 40
url: /net/aspose.words.vba/vbamodulecollection/remove/
---
## Remove method

Removes the specified module from the collection.

```csharp
public void Remove(VbaModule module)
```

| Parameter | Type | Description |
| --- | --- | --- |
| module | VbaModule | The module to remove. |

## Examples

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

* class [VbaModule](../../vbamodule/)
* class [VbaModuleCollection](../)
* namespace [Aspose.Words.Vba](../../vbamodulecollection/)
* assembly [Aspose.Words](../../../)
