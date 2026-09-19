---
title: "Aspose::Words::Vba::VbaModuleType enum"
linktitle: "VbaModuleType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Vba::VbaModuleType enum. Specifica il tipo di un modello in un progetto VBA in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enum


Specifica il tipo di modello in un progetto VBA.

```cpp
enum class VbaModuleType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| DocumentModule | 0 | Un tipo di elemento del progetto VBA che specifica un modulo per macro incorporate e operazioni di accesso programmatico associate a un documento. |
| ProceduralModule | 1 | Una raccolta di subroutine e funzioni. |
| ClassModule | 2 | Un modulo che contiene la definizione di un nuovo oggetto. Ogni istanza di una classe crea un nuovo oggetto, e le procedure definite nel modulo diventano proprietà e metodi dell'oggetto. |
| DesignerModule | 3 | Un modulo VBA che estende i metodi e le proprietà di un controllo ActiveX registrato nel progetto. |


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

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
