---
title: get_Type
second_title: Aspose.Words for C++ API Reference
description: Specifies whether the module is a procedural module, document module, class module, or designer module.
type: docs
weight: 66
url: /cpp/aspose.words.vba/vbamodule/get_type/
---
## VbaModule::get_Type method


Specifies whether the module is a procedural module, document module, class module, or designer module.

```cpp
Aspose::Words::Vba::VbaModuleType Aspose::Words::Vba::VbaModule::get_Type() const
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

* Enum [VbaModuleType](../../vbamoduletype/)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words](../../../)
