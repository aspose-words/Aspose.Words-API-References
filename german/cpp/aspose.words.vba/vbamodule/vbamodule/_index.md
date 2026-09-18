---
title: "Aspose::Words::Vba::VbaModule::VbaModule Konstruktor"
linktitle: "VbaModule"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Vba::VbaModule::VbaModule Konstruktor. Erstellt ein leeres Modul in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule::VbaModule constructor


Erstellt ein leeres Modul.

```cpp
Aspose::Words::Vba::VbaModule::VbaModule()
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

* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
