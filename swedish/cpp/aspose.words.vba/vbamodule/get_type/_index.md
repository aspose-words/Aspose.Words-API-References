---
title: "Aspose::Words::Vba::VbaModule::get_Type-metod"
linktitle: "get_Type"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Vba::VbaModule::get_Type-metod. Anger om modulen är en procedurmodul, dokumentmodul, klassmodul eller designermodul i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.vba/vbamodule/get_type/
---
## VbaModule::get_Type method


Anger om modulen är en procedurmodul, dokumentmodul, klassmodul eller designermodul.

```cpp
Aspose::Words::Vba::VbaModuleType Aspose::Words::Vba::VbaModule::get_Type() const
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

* Enum [VbaModuleType](../../vbamoduletype/)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
