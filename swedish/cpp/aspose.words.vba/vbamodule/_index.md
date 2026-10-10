---
title: "Aspose::Words::Vba::VbaModule class"
linktitle: "VbaModule"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Vba::VbaModule class. Tillhandahåller åtkomst till VBA-projektmodulen. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 1000
url: /sv/cpp/aspose.words.vba/vbamodule/
---
## VbaModule class


Ger åtkomst till VBA‑projektmodulen. För att lära dig mer, besök [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/) dokumentationsartikel.

```cpp
class VbaModule : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clone](./clone/)() | Utför en kopia av [VbaModule](./). |
| [get_Name](./get_name/)() const | Hämtar eller anger VBA-projektmodulens namn. |
| [get_SourceCode](./get_sourcecode/)() const | Hämtar eller anger VBA-projektmodulens källkod. |
| [get_Type](./get_type/)() const | Anger om modulen är en procedurmodul, dokumentmodul, klassmodul eller designermodul. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Name](./set_name/)(const System::String\&) | Sättare för [Aspose::Words::Vba::VbaModule::get_Name](./get_name/). |
| [set_SourceCode](./set_sourcecode/)(const System::String\&) | Sättare för [Aspose::Words::Vba::VbaModule::get_SourceCode](./get_sourcecode/). |
| [set_Type](./set_type/)(Aspose::Words::Vba::VbaModuleType) | Sättare för [Aspose::Words::Vba::VbaModule::get_Type](./get_type/). |
| static [Type](./type/)() |  |
| [VbaModule](./vbamodule/)() | Skapar en tom modul. |

## Exempel



Visar hur man får åtkomst till information om ett dokuments VBA-projekt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");

// Ett VBA-projekt innehåller en samling av VBA-moduler.
System::SharedPtr<Aspose::Words::Vba::VbaProject> vbaProject = doc->get_VbaProject();
std::cout << (vbaProject->get_IsSigned() ? System::String::Format(u"Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count()) : System::String::Format(u"Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count())) << std::endl;

System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> vbaModules = doc->get_VbaProject()->get_Modules();

ASSERT_EQ(vbaModules->LINQ_Count(), 3);

for (auto&& module_ : vbaModules)
{
    std::cout << System::String::Format(u"Module name: {0};\nModule code:\n{1}\n", module_->get_Name(), module_->get_SourceCode()) << std::endl;
}

// Ställ in ny källkod för VBA-modulen. Du kan komma åt VBA-moduler i samlingen antingen via index eller via namn.
vbaModules->idx_get(0)->set_SourceCode(u"Your VBA code...");
vbaModules->idx_get(u"Module1")->set_SourceCode(u"Your VBA code...");

// Ta bort en modul från samlingen.
vbaModules->Remove(vbaModules->idx_get(2));
```

## Se även

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
