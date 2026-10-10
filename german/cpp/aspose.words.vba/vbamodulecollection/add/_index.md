---
title: "Aspose::Words::Vba::VbaModuleCollection::Add‑Methode"
linktitle: "Add"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Vba::VbaModuleCollection::Add‑Methode. Fügt ein Modul zur Sammlung in C++ hinzu."
type: docs
weight: 2000
url: /de/cpp/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection::Add method


Fügt ein Modul zur Sammlung hinzu.

```cpp
void Aspose::Words::Vba::VbaModuleCollection::Add(const System::SharedPtr<Aspose::Words::Vba::VbaModule> &vbaModule)
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

* Class [VbaModule](../../vbamodule/)
* Class [VbaModuleCollection](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
