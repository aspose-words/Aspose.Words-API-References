---
title: VbaModuleType Enum
linktitle: VbaModuleType
articleTitle: VbaModuleType
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Vba.VbaModuleType enum, defining model types in VBA projects for enhanced automation and streamlined document management.
type: docs
weight: 7430
url: /net/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enumeration

Specifies the type of a model in a VBA project.

```csharp
public enum VbaModuleType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| DocumentModule | `0` | A type of VBA project item that specifies a module for embedded macros and programmatic access operations that are associated with a document. |
| ProceduralModule | `1` | A collection of subroutines and functions. |
| ClassModule | `2` | A module that contains the definition for a new object. Each instance of a class creates a new object, and procedures that are defined in the module become properties and methods of the object. |
| DesignerModule | `3` | A VBA module that extends the methods and properties of an ActiveX control that has been registered with the project. |

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

* namespace [Aspose.Words.Vba](../../aspose.words.vba/)
* assembly [Aspose.Words](../../)
