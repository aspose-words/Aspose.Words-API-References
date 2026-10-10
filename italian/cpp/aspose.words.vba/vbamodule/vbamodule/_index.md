---
title: "Aspose::Words::Vba::VbaModule::VbaModule costruttore"
linktitle: "VbaModule"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Vba::VbaModule::VbaModule costruttore. Crea un modulo vuoto in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule::VbaModule constructor


Crea un modulo vuoto.

```cpp
Aspose::Words::Vba::VbaModule::VbaModule()
```


## Esempi



Mostra come creare un progetto VBA utilizzando le macro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea un nuovo progetto VBA.
auto project = System::MakeObject<Aspose::Words::Vba::VbaProject>();
project->set_Name(u"Aspose.Project");
doc->set_VbaProject(project);

// Crea un nuovo modulo e specifica il codice sorgente di una macro.
auto module_ = System::MakeObject<Aspose::Words::Vba::VbaModule>();
module_->set_Name(u"Aspose.Module");
module_->set_Type(Aspose::Words::Vba::VbaModuleType::ProceduralModule);
module_->set_SourceCode(u"New source code");

// Aggiungi il modulo al progetto VBA.
doc->get_VbaProject()->get_Modules()->Add(module_);

doc->Save(get_ArtifactsDir() + u"VbaProject.CreateVBAMacros.docm");
```

## Vedi anche

* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
