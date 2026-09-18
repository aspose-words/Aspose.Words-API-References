---
title: "Aspose::Words::Vba::VbaProject Klasse"
linktitle: "VbaProject"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Vba::VbaProject Klasse. Bietet Zugriff auf VBA-Projektinformationen. Ein VBA-Projekt im Dokument wird als Sammlung von VBA-Modulen definiert. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.vba/vbaproject/
---
## VbaProject class


Bietet Zugriff auf VBA‑Projektdaten. Ein VBA‑Projekt im Dokument ist als Sammlung von VBA‑Modulen definiert. Weitere Informationen finden Sie im Dokumentationsartikel [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaProject : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Clone](./clone/)() | Führt eine Kopie des [VbaProject](./) aus. |
| [get_CodePage](./get_codepage/)() const | Liest oder setzt die Codepage des VBA-Projekts. |
| [get_IsProtected](./get_isprotected/)() | Zeigt an, ob das [VbaProject](./) passwortgeschützt ist. |
| [get_IsSigned](./get_issigned/)() | Zeigt an, ob das [VbaProject](./) signiert ist oder nicht. |
| [get_Modules](./get_modules/)() | Gibt die Sammlung von VBA-Projektmodulen zurück. |
| [get_Name](./get_name/)() const | Liest oder setzt den Namen des VBA-Projekts. |
| [get_References](./get_references/)() | Liefert eine Sammlung von VBA-Projektreferenzen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CodePage](./set_codepage/)(int32_t) | Setter für [Aspose::Words::Vba::VbaProject::get_CodePage](./get_codepage/). |
| [set_Name](./set_name/)(const System::String\&) | Setter für [Aspose::Words::Vba::VbaProject::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [VbaProject](./vbaproject/)() | Erstellt ein leeres [VbaProject](./). |

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
