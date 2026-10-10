---
title: "Aspose::Words::Vba::VbaModuleType enum"
linktitle: "VbaModuleType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Vba::VbaModuleType enum. Anger typen av en modell i ett VBA-projekt i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enum


Anger typen av en modell i ett VBA-projekt.

```cpp
enum class VbaModuleType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| DocumentModule | 0 | En typ av VBA-projektobjekt som anger en modul för inbäddade makron och programmatisk åtkomst som är associerade med ett dokument. |
| ProceduralModule | 1 | En samling av subrutiner och funktioner. |
| ClassModule | 2 | En modul som innehåller definitionen för ett nytt objekt. Varje instans av en klass skapar ett nytt objekt, och procedurer som definieras i modulen blir egenskaper och metoder för objektet. |
| DesignerModule | 3 | En VBA-modul som utökar metoderna och egenskaperna hos en ActiveX-kontroll som har registrerats i projektet. |


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

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
