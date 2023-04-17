---
title: VbaModuleType enumeration
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the type of a model in a VBA project."
type: docs
weight: 40
url: /python-net/aspose.words.vba/vbamoduletype/
---

## VbaModuleType enumeration

Specifies the type of a model in a VBA project.


### Members

| Name | Description |
| --- | --- |
| DOCUMENT_MODULE | A type of VBA project item that specifies a module for embedded macros and programmatic access operations  that are associated with a document. |
| PROCEDURAL_MODULE | A collection of subroutines and functions. |
| CLASS_MODULE | A module that contains the definition for a new object. Each instance of a class creates a new object, and procedures that are defined in the module become properties and methods of the object. |
| DESIGNER_MODULE | A VBA module that extends the methods and properties of an ActiveX control that has been registered with the project. |

### Examples

Shows how to create a VBA project using macros.

```python
doc = aw.Document()

# Create a new VBA project.
project = aw.vba.VbaProject()
project.name = "Aspose.Project"
doc.vba_project = project

# Create a new module and specify a macro source code.
module = aw.vba.VbaModule()
module.name = "Aspose.Module"
module.type = aw.vba.VbaModuleType.PROCEDURAL_MODULE
module.source_code = "New source code"

# Add the module to the VBA project.
doc.vba_project.modules.add(module)

doc.save(ARTIFACTS_DIR + "VbaProject.create_new_vba_project.docm")
```

### See Also

* module [aspose.words.vba](../)

