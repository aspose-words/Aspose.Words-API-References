---
title: Aspose::Words::Vba::VbaModuleCollection::Add method
linktitle: Add
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Vba::VbaModuleCollection::Add method. Adds a module to the collection in C++.'
type: docs
weight: 2000
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
auto doc = System::MakeObject<Aspose::Words::Document>();

// Create a new VBA project.
auto project = System::MakeObject<Aspose::Words::Vba::VbaProject>();
project->set_Name(u"Aspose.Project");
doc->set_VbaProject(project);

// Create a new module and specify a macro source code.
auto module_ = System::MakeObject<Aspose::Words::Vba::VbaModule>();
module_->set_Name(u"Aspose.Module");
module_->set_Type(Aspose::Words::Vba::VbaModuleType::ProceduralModule);
module_->set_SourceCode(u"New source code");

// Add the module to the VBA project.
doc->get_VbaProject()->get_Modules()->Add(module_);

doc->Save(get_ArtifactsDir() + u"VbaProject.CreateVBAMacros.docm");
```

## See Also

* Class [VbaModule](../../vbamodule/)
* Class [VbaModuleCollection](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
