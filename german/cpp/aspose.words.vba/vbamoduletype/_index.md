---
title: "Aspose::Words::Vba::VbaModuleType enum"
linktitle: "VbaModuleType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Vba::VbaModuleType enum. Gibt den Typ eines Modells in einem VBA-Projekt in C++ an."
type: docs
weight: 6000
url: /de/cpp/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enum


Gibt den Typ eines Modells in einem VBA‑Projekt an.

```cpp
enum class VbaModuleType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| DocumentModule | 0 | Ein Typ von VBA-Projekt-Element, das ein Modul für eingebettete Makros und programmatischen Zugriffsoperationen angibt, die mit einem Dokument verknüpft sind. |
| ProceduralModule | 1 | Eine Sammlung von Unterroutinen und Funktionen. |
| ClassModule | 2 | Ein Modul, das die Definition für ein neues Objekt enthält. Jede Instanz einer Klasse erzeugt ein neues Objekt, und in dem Modul definierte Prozeduren werden zu Eigenschaften und Methoden des Objekts. |
| DesignerModule | 3 | Ein VBA-Modul, das die Methoden und Eigenschaften eines ActiveX-Steuerelements erweitert, das im Projekt registriert wurde. |


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

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
