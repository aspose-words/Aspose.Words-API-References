---
title: Aspose::Words::Vba::VbaProject::VbaProject constructor
linktitle: VbaProject
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Vba::VbaProject::VbaProject constructor. Creates a blank VbaProject in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject::VbaProject constructor


Creates a blank [VbaProject](../).

```cpp
Aspose::Words::Vba::VbaProject::VbaProject()
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

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
