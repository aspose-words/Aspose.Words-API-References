---
title: "Metodo Aspose::Words::Vba::VbaModule::get_Type"
linktitle: "get_Type"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Vba::VbaModule::get_Type. Specifica se il modulo è un modulo procedurale, modulo documento, modulo classe o modulo designer in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.vba/vbamodule/get_type/
---
## VbaModule::get_Type method


Specifica se il modulo è un modulo procedurale, modulo documento, modulo classe o modulo designer.

```cpp
Aspose::Words::Vba::VbaModuleType Aspose::Words::Vba::VbaModule::get_Type() const
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

* Enum [VbaModuleType](../../vbamoduletype/)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
