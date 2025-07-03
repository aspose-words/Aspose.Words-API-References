---
title: Aspose::Words::Document::get_VbaProject method
linktitle: get_VbaProject
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_VbaProject method. Gets or sets a VbaProject in C++.'
type: docs
weight: 56000
url: /cpp/aspose.words/document/get_vbaproject/
---
## Document::get_VbaProject method


Gets or sets a [VbaProject](./).

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaProject> Aspose::Words::Document::get_VbaProject() const
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

## See Also

* Class [VbaProject](../../../aspose.words.vba/vbaproject/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
