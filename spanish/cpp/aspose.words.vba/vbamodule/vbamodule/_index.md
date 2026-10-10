---
title: "Aspose::Words::Vba::VbaModule::VbaModule constructor"
linktitle: "VbaModule"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Vba::VbaModule::VbaModule constructor. Crea un módulo vacío en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule::VbaModule constructor


Crea un módulo vacío.

```cpp
Aspose::Words::Vba::VbaModule::VbaModule()
```


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

* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
