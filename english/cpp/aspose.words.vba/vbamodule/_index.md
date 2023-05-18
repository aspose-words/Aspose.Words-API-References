---
title: Aspose::Words::Vba::VbaModule class
linktitle: VbaModule
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Vba::VbaModule class. Provides access to VBA project module. To learn more, visit the  documentation article in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.vba/vbamodule/
---
## VbaModule class


Provides access to VBA project module. To learn more, visit the [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/) documentation article.

```cpp
class VbaModule : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Clone](./clone/)() | Performs a copy of the [VbaModule](./). |
| [get_Name](./get_name/)() const | Gets or sets VBA project module name. |
| [get_SourceCode](./get_sourcecode/)() const | Gets or sets VBA project module source code. |
| [get_Type](./get_type/)() const | Specifies whether the module is a procedural module, document module, class module, or designer module. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Name](./set_name/)(const System::String\&) | Setter for [Aspose::Words::Vba::VbaModule::get_Name](./get_name/). |
| [set_SourceCode](./set_sourcecode/)(const System::String\&) | Setter for [Aspose::Words::Vba::VbaModule::get_SourceCode](./get_sourcecode/). |
| [set_Type](./set_type/)(Aspose::Words::Vba::VbaModuleType) | Setter for [Aspose::Words::Vba::VbaModule::get_Type](./get_type/). |
| static [Type](./type/)() |  |
| [VbaModule](./vbamodule/)() | Creates an empty module. |

## Examples



Shows how to access a document's VBA project information. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"VBA project.docm");

// A VBA project contains a collection of VBA modules.
SharedPtr<VbaProject> vbaProject = doc->get_VbaProject();
std::cout << (vbaProject->get_IsSigned() ? String::Format(u"Project name: {0} signed; Project code page: {1}; Modules count: {2}\n",
                                                          vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count())
                                         : String::Format(u"Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n",
                                                          vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count()))
          << std::endl;

SharedPtr<VbaModuleCollection> vbaModules = doc->get_VbaProject()->get_Modules();

ASSERT_EQ(vbaModules->LINQ_Count(), 3);

for (const auto& module_ : vbaModules)
{
    std::cout << "Module name: " << module_->get_Name() << ";\nModule code:\n" << module_->get_SourceCode() << "\n" << std::endl;
}

// Set new source code for VBA module. You can access VBA modules in the collection either by index or by name.
vbaModules->idx_get(0)->set_SourceCode(u"Your VBA code...");
vbaModules->idx_get(u"Module1")->set_SourceCode(u"Your VBA code...");

// Remove a module from the collection.
vbaModules->Remove(vbaModules->idx_get(2));
```

## See Also

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
