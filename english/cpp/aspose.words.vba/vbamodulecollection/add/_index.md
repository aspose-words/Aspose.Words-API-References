---
title: Add
second_title: Aspose.Words for C++ API Reference
description: Adds a module to the collection.
type: docs
weight: 14
url: /cpp/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection::Add method


Adds a module to the collection.

```cpp
void Aspose::Words::Vba::VbaModuleCollection::Add(const System::SharedPtr<Aspose::Words::Vba::VbaModule> &vbaModule)
```


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

* Class [VbaModule](../../vbamodule/)
* Class [VbaModuleCollection](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words](../../../)
