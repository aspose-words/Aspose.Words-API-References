---
title: "Aspose::Words::Vba::VbaModule::get_Type Methode"
linktitle: "get_Type"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Vba::VbaModule::get_Type method. Gibt an, ob das Modul ein prozedurales Modul, Dokumentmodul, Klassenmodul oder Designer‑Modul in C++ ist."
type: docs
weight: 6000
url: /de/cpp/aspose.words.vba/vbamodule/get_type/
---
## VbaModule::get_Type method


Gibt an, ob das Modul ein Prozedurmodul, Dokumentmodul, Klassenmodul oder Designer‑Modul ist.

```cpp
Aspose::Words::Vba::VbaModuleType Aspose::Words::Vba::VbaModule::get_Type() const
```


## Beispiele



Zeigt, wie man ein VBA-Projekt mit Makros erstellt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Erstelle ein neues VBA-Projekt.
auto project = System::MakeObject<Aspose::Words::Vba::VbaProject>();
project->set_Name(u"Aspose.Project");
doc->set_VbaProject(project);

// Erstelle ein neues Modul und gib einen Makro-Quellcode an.
auto module_ = System::MakeObject<Aspose::Words::Vba::VbaModule>();
module_->set_Name(u"Aspose.Module");
module_->set_Type(Aspose::Words::Vba::VbaModuleType::ProceduralModule);
module_->set_SourceCode(u"New source code");

// Füge das Modul dem VBA-Projekt hinzu.
doc->get_VbaProject()->get_Modules()->Add(module_);

doc->Save(get_ArtifactsDir() + u"VbaProject.CreateVBAMacros.docm");
```

## Siehe auch

* Enum [VbaModuleType](../../vbamoduletype/)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
