---
title: VbaModuleCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: Access VbaModule objects effortlessly with the VbaModuleCollection Item property. Enhance your VBA projects with easy indexing and improved management.
type: docs
weight: 20
url: /net/aspose.words.vba/vbamodulecollection/item/
---
## VbaModuleCollection indexer (1 of 2)

Retrieves a [`VbaModule`](../../vbamodule/) object by index.

```csharp
public VbaModule this[int index] { get; }
```

| Parameter | Description |
| --- | --- |
| index | Zero-based index of the module to retrieve. |

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

Assert.That(3, Is.EqualTo(vbaModules.Count()));

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
* namespace [Aspose.Words.Vba](../../../aspose.words.vba/)
* assembly [Aspose.Words](../../../)

---

## VbaModuleCollection indexer (2 of 2)

Retrieves a [`VbaModule`](../../vbamodule/) object by name, or Null if not found.

```csharp
public VbaModule this[string name] { get; }
```

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

Assert.That(3, Is.EqualTo(vbaModules.Count()));

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
* namespace [Aspose.Words.Vba](../../../aspose.words.vba/)
* assembly [Aspose.Words](../../../)
