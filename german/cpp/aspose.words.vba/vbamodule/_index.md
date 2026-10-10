---
title: "Aspose::Words::Vba::VbaModule class"
linktitle: "VbaModule"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Vba::VbaModule class. Stellt Zugriff auf das VBA-Projektmodul bereit. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.vba/vbamodule/
---
## VbaModule class


Bietet Zugriff auf das VBA‑Projektmodul. Weitere Informationen finden Sie im Dokumentationsartikel [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaModule : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clone](./clone/)() | Führt eine Kopie des [VbaModule](./) aus. |
| [get_Name](./get_name/)() const | Liest oder setzt den Namen des VBA-Projektmoduls. |
| [get_SourceCode](./get_sourcecode/)() const | Liest oder setzt den Quellcode des VBA-Projektmoduls. |
| [get_Type](./get_type/)() const | Gibt an, ob das Modul ein Prozedurmodul, Dokumentmodul, Klassenmodul oder Designer‑Modul ist. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Name](./set_name/)(const System::String\&) | Setter für [Aspose::Words::Vba::VbaModule::get_Name](./get_name/). |
| [set_SourceCode](./set_sourcecode/)(const System::String\&) | Setter für [Aspose::Words::Vba::VbaModule::get_SourceCode](./get_sourcecode/). |
| [set_Type](./set_type/)(Aspose::Words::Vba::VbaModuleType) | Setter für [Aspose::Words::Vba::VbaModule::get_Type](./get_type/). |
| static [Type](./type/)() |  |
| [VbaModule](./vbamodule/)() | Erstellt ein leeres Modul. |

## Beispiele



Zeigt, wie man auf die VBA-Projektinformationen eines Dokuments zugreift.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");

// Ein VBA-Projekt enthält eine Sammlung von VBA-Modulen.
System::SharedPtr<Aspose::Words::Vba::VbaProject> vbaProject = doc->get_VbaProject();
std::cout << (vbaProject->get_IsSigned() ? System::String::Format(u"Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count()) : System::String::Format(u"Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count())) << std::endl;

System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> vbaModules = doc->get_VbaProject()->get_Modules();

ASSERT_EQ(vbaModules->LINQ_Count(), 3);

for (auto&& module_ : vbaModules)
{
    std::cout << System::String::Format(u"Module name: {0};\nModule code:\n{1}\n", module_->get_Name(), module_->get_SourceCode()) << std::endl;
}

// Setzt neuen Quellcode für ein VBA-Modul. Sie können auf VBA-Module in der Sammlung entweder über den Index oder über den Namen zugreifen.
vbaModules->idx_get(0)->set_SourceCode(u"Your VBA code...");
vbaModules->idx_get(u"Module1")->set_SourceCode(u"Your VBA code...");

// Entfernt ein Modul aus der Sammlung.
vbaModules->Remove(vbaModules->idx_get(2));
```

## Siehe auch

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
