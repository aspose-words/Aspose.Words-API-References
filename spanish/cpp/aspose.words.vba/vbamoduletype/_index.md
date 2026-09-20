---
title: "Aspose::Words::Vba::VbaModuleType enumeración"
linktitle: "VbaModuleType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Vba::VbaModuleType enumeración. Especifica el tipo de un modelo en un proyecto VBA en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enum


Especifica el tipo de un modelo en un proyecto VBA.

```cpp
enum class VbaModuleType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| DocumentModule | 0 | Un tipo de elemento de proyecto VBA que especifica un módulo para macros incrustados y operaciones de acceso programático asociadas a un documento. |
| ProceduralModule | 1 | Una colección de subrutinas y funciones. |
| ClassModule | 2 | Un módulo que contiene la definición de un nuevo objeto. Cada instancia de una clase crea un nuevo objeto, y los procedimientos que se definen en el módulo se convierten en propiedades y métodos del objeto. |
| DesignerModule | 3 | Un módulo VBA que amplía los métodos y propiedades de un control ActiveX que ha sido registrado en el proyecto. |


## Ejemplos



Muestra cómo crear un proyecto VBA usando macros.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea un nuevo proyecto VBA.
auto project = System::MakeObject<Aspose::Words::Vba::VbaProject>();
project->set_Name(u"Aspose.Project");
doc->set_VbaProject(project);

// Crea un nuevo módulo y especifica el código fuente de una macro.
auto module_ = System::MakeObject<Aspose::Words::Vba::VbaModule>();
module_->set_Name(u"Aspose.Module");
module_->set_Type(Aspose::Words::Vba::VbaModuleType::ProceduralModule);
module_->set_SourceCode(u"New source code");

// Agrega el módulo al proyecto VBA.
doc->get_VbaProject()->get_Modules()->Add(module_);

doc->Save(get_ArtifactsDir() + u"VbaProject.CreateVBAMacros.docm");
```

## Ver también

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
