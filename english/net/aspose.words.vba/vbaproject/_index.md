---
title: VbaProject Class
linktitle: VbaProject
articleTitle: VbaProject
second_title: Aspose.Words for .NET
description: Unlock the power of Aspose.Words.Vba.VbaProject class to effortlessly manage VBA project info and modules within your documents. Enhance your automation today!
type: docs
weight: 7520
url: /net/aspose.words.vba/vbaproject/
---
## VbaProject class

Provides access to VBA project information. A VBA project inside the document is defined as a collection of VBA modules.

To learn more, visit the [Working with VBA Macros](https://docs.aspose.com/words/net/working-with-vba-macros/) documentation article.

```csharp
public class VbaProject
```

## Constructors

| Name | Description |
| --- | --- |
| [VbaProject](vbaproject/)() | Creates a blank `VbaProject`. |

## Properties

| Name | Description |
| --- | --- |
| [CodePage](../../aspose.words.vba/vbaproject/codepage/) { get; set; } | Gets or sets the VBA project’s code page. |
| [IsProtected](../../aspose.words.vba/vbaproject/isprotected/) { get; } | Shows whether the `VbaProject` is password protected. |
| [IsSigned](../../aspose.words.vba/vbaproject/issigned/) { get; } | Shows whether the `VbaProject` is signed or not. |
| [Modules](../../aspose.words.vba/vbaproject/modules/) { get; } | Returns collection of VBA project modules. |
| [Name](../../aspose.words.vba/vbaproject/name/) { get; set; } | Gets or sets VBA project name. |
| [References](../../aspose.words.vba/vbaproject/references/) { get; } | Gets a collection of VBA project references. |

## Methods

| Name | Description |
| --- | --- |
| [Clone](../../aspose.words.vba/vbaproject/clone/)() | Performs a copy of the `VbaProject`. |

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

* namespace [Aspose.Words.Vba](../../aspose.words.vba/)
* assembly [Aspose.Words](../../)
