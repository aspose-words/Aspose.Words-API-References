---
title: "Aspose::Words::Vba::VbaProject klass"
linktitle: "VbaProject"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Vba::VbaProject klass. Ger åtkomst till information om VBA-projekt. Ett VBA-projekt i dokumentet definieras som en samling av VBA-moduler. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.vba/vbaproject/
---
## VbaProject class


Tillhandahåller åtkomst till information om VBA-projekt. Ett VBA-projekt i dokumentet definieras som en samling av VBA-moduler. För att lära dig mer, besök dokumentationsartikeln [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaProject : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Clone](./clone/)() | Utför en kopia av [VbaProject](./). |
| [get_CodePage](./get_codepage/)() const | Hämtar eller anger VBA-projektets kodsida. |
| [get_IsProtected](./get_isprotected/)() | Visar om [VbaProject](./) är lösenordsskyddat. |
| [get_IsSigned](./get_issigned/)() | Visar om [VbaProject](./) är signerat eller inte. |
| [get_Modules](./get_modules/)() | Returnerar en samling av VBA-projektmoduler. |
| [get_Name](./get_name/)() const | Hämtar eller anger VBA-projektnamn. |
| [get_References](./get_references/)() | Hämtar en samling av VBA-projektreferenser. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CodePage](./set_codepage/)(int32_t) | Sättare för [Aspose::Words::Vba::VbaProject::get_CodePage](./get_codepage/). |
| [set_Name](./set_name/)(const System::String\&) | Sättare för [Aspose::Words::Vba::VbaProject::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [VbaProject](./vbaproject/)() | Skapar ett tomt [VbaProject](./). |

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
