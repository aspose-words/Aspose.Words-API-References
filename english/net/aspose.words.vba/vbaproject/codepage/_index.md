---
title: VbaProject.CodePage
linktitle: CodePage
second_title: Aspose.Words for .NET API Reference
description: VbaProject CodePage property. Gets or sets the VBA projects code page in C#.
type: docs
weight: 20
url: /net/aspose.words.vba/vbaproject/codepage/
---
## VbaProject.CodePage property

Gets or sets the VBA project’s code page.

```csharp
public int CodePage { get; set; }
```

## Remarks

Please note that VBA is pre-Unicode feature and you have to explicitly set appropriate code page to preserve regional character sets.

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

* class [VbaProject](../)
* namespace [Aspose.Words.Vba](../../vbaproject/)
* assembly [Aspose.Words](../../../)
