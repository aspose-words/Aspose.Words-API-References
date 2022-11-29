---
title: VbaProject
second_title: Aspose.Words for C++ API Reference
description: Creates a blank VbaProject.
type: docs
weight: 1
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

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words](../../../)
