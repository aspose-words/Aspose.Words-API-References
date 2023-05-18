---
title: Aspose::Words::Vba::VbaModuleType enum
linktitle: VbaModuleType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Vba::VbaModuleType enum. Specifies the type of a model in a VBA project in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enum


Specifies the type of a model in a VBA project.

```cpp
enum class VbaModuleType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| DocumentModule | 0 | A type of VBA project item that specifies a module for embedded macros and programmatic access operations that are associated with a document. |
| ProceduralModule | 1 | A collection of subroutines and functions. |
| ClassModule | 2 | A module that contains the definition for a new object. Each instance of a class creates a new object, and procedures that are defined in the module become properties and methods of the object. |
| DesignerModule | 3 | A VBA module that extends the methods and properties of an ActiveX control that has been registered with the project. |


## Examples



Shows how to create a VBA project using macros. 
```cpp
auto doc = MakeObject<Document>();

// Create a new VBA project.
auto project = MakeObject<VbaProject>();
project->set_Name(u"Aspose.Project");
doc->set_VbaProject(project);

// Create a new module and specify a macro source code.
auto module_ = MakeObject<VbaModule>();
module_->set_Name(u"Aspose.Module");
module_->set_Type(VbaModuleType::ProceduralModule);
module_->set_SourceCode(u"New source code");

// Add the module to the VBA project.
doc->get_VbaProject()->get_Modules()->Add(module_);

doc->Save(ArtifactsDir + u"VbaProject.CreateVBAMacros.docm");
```

## See Also

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
