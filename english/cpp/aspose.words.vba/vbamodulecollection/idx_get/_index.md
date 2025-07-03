---
title: Aspose::Words::Vba::VbaModuleCollection::idx_get method
linktitle: idx_get
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Vba::VbaModuleCollection::idx_get method. Retrieves a VbaModule object by name, or Null if not found in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.vba/vbamodulecollection/idx_get/
---
## VbaModuleCollection::idx_get(const System::String\&) method


Retrieves a [VbaModule](../../vbamodule/) object by name, or Null if not found.

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModule> Aspose::Words::Vba::VbaModuleCollection::idx_get(const System::String &name)
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

* Class [VbaModule](../../vbamodule/)
* Class [VbaModuleCollection](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
## VbaModuleCollection::idx_get(int32_t) method


Retrieves a [VbaModule](../../vbamodule/) object by index.

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModule> Aspose::Words::Vba::VbaModuleCollection::idx_get(int32_t index)
```


| Parameter | Type | Description |
| --- | --- | --- |
| index | int32_t | Zero-based index of the module to retrieve. |

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

* Class [VbaModule](../../vbamodule/)
* Class [VbaModuleCollection](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
