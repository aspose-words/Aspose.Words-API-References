---
title: Aspose::Words::Vba::VbaModule::get_Name method
linktitle: get_Name
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Vba::VbaModule::get_Name method. Gets or sets VBA project module name in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.vba/vbamodule/get_name/
---
## VbaModule::get_Name method


Gets or sets VBA project module name.

```cpp
System::String Aspose::Words::Vba::VbaModule::get_Name() const
```


## Examples



Shows how to access a document's VBA project information. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");

// A VBA project contains a collection of VBA modules.
System::SharedPtr<Aspose::Words::Vba::VbaProject> vbaProject = doc->get_VbaProject();
std::cout << (vbaProject->get_IsSigned() ? System::String::Format(u"Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count()) : System::String::Format(u"Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count())) << std::endl;

System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> vbaModules = doc->get_VbaProject()->get_Modules();

ASSERT_EQ(vbaModules->LINQ_Count(), 3);

for (auto&& module_ : vbaModules)
{
    std::cout << System::String::Format(u"Module name: {0};\nModule code:\n{1}\n", module_->get_Name(), module_->get_SourceCode()) << std::endl;
}

// Set new source code for VBA module. You can access VBA modules in the collection either by index or by name.
vbaModules->idx_get(0)->set_SourceCode(u"Your VBA code...");
vbaModules->idx_get(u"Module1")->set_SourceCode(u"Your VBA code...");

// Remove a module from the collection.
vbaModules->Remove(vbaModules->idx_get(2));
```


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

* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
