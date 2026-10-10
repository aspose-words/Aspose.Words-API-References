---
title: "Aspose::Words::Vba::VbaProject::get_Modules Methode"
linktitle: "get_Modules"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Vba::VbaProject::get_Modules Methode. Gibt eine Sammlung von VBA-Projektmodulen in C++ zurück."
type: docs
weight: 6000
url: /de/cpp/aspose.words.vba/vbaproject/get_modules/
---
## VbaProject::get_Modules method


Gibt die Sammlung von VBA-Projektmodulen zurück.

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> Aspose::Words::Vba::VbaProject::get_Modules()
```


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

* Class [VbaModuleCollection](../../vbamodulecollection/)
* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
