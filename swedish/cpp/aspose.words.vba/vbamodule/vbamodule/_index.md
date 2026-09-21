---
title: "Aspose::Words::Vba::VbaModule::VbaModule konstruktor"
linktitle: "VbaModule"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Vba::VbaModule::VbaModule konstruktor. Skapar en tom modul i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule::VbaModule constructor


Skapar en tom modul.

```cpp
Aspose::Words::Vba::VbaModule::VbaModule()
```


## Exempel



Visar hur man skapar ett VBA-projekt med makron.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa ett nytt VBA-projekt.
auto project = System::MakeObject<Aspose::Words::Vba::VbaProject>();
project->set_Name(u"Aspose.Project");
doc->set_VbaProject(project);

// Skapa en ny modul och ange makrokällkod.
auto module_ = System::MakeObject<Aspose::Words::Vba::VbaModule>();
module_->set_Name(u"Aspose.Module");
module_->set_Type(Aspose::Words::Vba::VbaModuleType::ProceduralModule);
module_->set_SourceCode(u"New source code");

// Lägg till modulen i VBA-projektet.
doc->get_VbaProject()->get_Modules()->Add(module_);

doc->Save(get_ArtifactsDir() + u"VbaProject.CreateVBAMacros.docm");
```

## Se även

* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
