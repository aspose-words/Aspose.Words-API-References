---
title: "Aspose::Words::Vba::VbaModuleCollection Klasse"
linktitle: "VbaModuleCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Vba::VbaModuleCollection Klasse. Stellt eine Sammlung von VbaModule‑Objekten dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.vba/vbamodulecollection/
---
## VbaModuleCollection class


Stellt eine Sammlung von [VbaModule](../vbamodule/)‑Objekten dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaModuleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Vba::VbaModule>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Vba::VbaModule\>\&) | Fügt ein Modul zur Sammlung hinzu. |
| [begin](./begin/)() |  |
| [begin](./begin/)() const |  |
| [cbegin](./cbegin/)() const |  |
| [cend](./cend/)() const |  |
| [end](./end/)() |  |
| [end](./end/)() const |  |
| [get_Count](./get_count/)() | Gibt die Anzahl der VBA-Module in der Sammlung zurück. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ruft ein [VbaModule](../vbamodule/)‑Objekt über den Index ab. |
| [idx_get](./idx_get/)(const System::String\&) | Ruft ein [VbaModule](../vbamodule/)‑Objekt über den Namen ab oder Null, wenn nicht gefunden. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Vba::VbaModule\>\&) | Entfernt das angegebene Modul aus der Sammlung. |
| static [Type](./type/)() |  |
| [virtualizeBeginConstIterator](./virtualizebeginconstiterator/)() const override |  |
| [virtualizeBeginIterator](./virtualizebeginiterator/)() override |  |
| [virtualizeEndConstIterator](./virtualizeendconstiterator/)() const override |  |
| [virtualizeEndIterator](./virtualizeenditerator/)() override |  |
## Typedefs

| Typedef | Beschreibung |
| --- | --- |
| [const_iterator](./const_iterator/) |  |
| [iterator](./iterator/) |  |
| [iterator_holder_type](./iterator_holder_type/) |  |
| [virtualized_iterator](./virtualized_iterator/) |  |
| [virtualized_iterator_element](./virtualized_iterator_element/) |  |

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
