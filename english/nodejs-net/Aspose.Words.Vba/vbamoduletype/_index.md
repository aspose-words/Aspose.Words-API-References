---
title: VbaModuleType enumeration
linktitle: VbaModuleType enumeration
articleTitle: VbaModuleType enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Vba.VbaModuleType enumeration. Specifies the type of a model in a VBA project."
type: docs
weight: 20
url: /nodejs-net/aspose.words.vba/vbamoduletype/
---

## VbaModuleType enumeration

Specifies the type of a model in a VBA project.


### Members

| Name | Description |
| --- | --- |
| DocumentModule | A type of VBA project item that specifies a module for embedded macros and programmatic access operations  that are associated with a document. |
| ProceduralModule | A collection of subroutines and functions. |
| ClassModule | A module that contains the definition for a new object. Each instance of a class creates a new object, and procedures that are defined in the module become properties and methods of the object. |
| DesignerModule | A VBA module that extends the methods and properties of an ActiveX control that has been registered with the project. |

### Examples

Shows how to create a VBA project using macros.

```js
let doc = new aw.Document();

// Create a new VBA project.
let project = new aw.Vba.VbaProject();
project.name = "Aspose.project";
doc.vbaProject = project;

// Create a new module and specify a macro source code.
let module = new aw.Vba.VbaModule();
module.name = "Aspose.Module";
module.type = aw.Vba.VbaModuleType.ProceduralModule;
module.sourceCode = "New source code";

// Add the module to the VBA project.
doc.vbaProject.modules.add(module);

doc.save(base.artifactsDir + "VbaProject.CreateVBAMacros.docm");
```

### See Also

* module [Aspose.Words.Vba](../)

