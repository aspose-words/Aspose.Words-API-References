---
title: Aspose::Words::Vba::VbaProject class
linktitle: VbaProject
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Vba::VbaProject class. Provides access to VBA project information. A VBA project inside the document is defined as a collection of VBA modules. To learn more, visit the  documentation article in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.vba/vbaproject/
---
## VbaProject class


Provides access to VBA project information. A VBA project inside the document is defined as a collection of VBA modules. To learn more, visit the [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/) documentation article.

```cpp
class VbaProject : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [Clone](./clone/)() | Performs a copy of the [VbaProject](./). |
| [get_CodePage](./get_codepage/)() const | Gets or sets the VBA project’s code page. |
| [get_IsProtected](./get_isprotected/)() |  |
| [get_IsSigned](./get_issigned/)() | Shows whether the [VbaProject](./) is signed or not. |
| [get_Modules](./get_modules/)() | Returns collection of VBA project modules. |
| [get_Name](./get_name/)() const | Gets or sets VBA project name. |
| [get_References](./get_references/)() | Gets a collection of VBA project references. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CodePage](./set_codepage/)(int32_t) | Setter for [Aspose::Words::Vba::VbaProject::get_CodePage](./get_codepage/). |
| [set_Name](./set_name/)(const System::String\&) | Setter for [Aspose::Words::Vba::VbaProject::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [VbaProject](./vbaproject/)() | Creates a blank [VbaProject](./). |

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
