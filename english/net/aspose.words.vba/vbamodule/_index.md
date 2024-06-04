---
title: VbaModule Class
linktitle: VbaModule
articleTitle: VbaModule
second_title: Aspose.Words for .NET
description: Aspose.Words.Vba.VbaModule class. Provides access to VBA project module in C#.
type: docs
weight: 6820
url: /net/aspose.words.vba/vbamodule/
---
## VbaModule class

Provides access to VBA project module.

To learn more, visit the [Working with VBA Macros](https://docs.aspose.com/words/net/working-with-vba-macros/) documentation article.

```csharp
public class VbaModule
```

## Constructors

| Name | Description |
| --- | --- |
| [VbaModule](vbamodule/)() | Creates an empty module. |

## Properties

| Name | Description |
| --- | --- |
| [Name](../../aspose.words.vba/vbamodule/name/) { get; set; } | Gets or sets VBA project module name. |
| [SourceCode](../../aspose.words.vba/vbamodule/sourcecode/) { get; set; } | Gets or sets VBA project module source code. |
| [Type](../../aspose.words.vba/vbamodule/type/) { get; set; } | Specifies whether the module is a procedural module, document module, class module, or designer module. |

## Methods

| Name | Description |
| --- | --- |
| [Clone](../../aspose.words.vba/vbamodule/clone/)() | Performs a copy of the `VbaModule`. |

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

* namespace [Aspose.Words.Vba](../../aspose.words.vba/)
* assembly [Aspose.Words](../../)
