---
title: "Aspose::Words::Vba::VbaModule::VbaModule конструктор"
linktitle: "VbaModule"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Vba::VbaModule::VbaModule конструктор. Создает пустой модуль в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.vba/vbamodule/vbamodule/
---
## VbaModule::VbaModule constructor


Создаёт пустой модуль.

```cpp
Aspose::Words::Vba::VbaModule::VbaModule()
```


## Примеры



Показывает, как создать проект VBA с использованием макросов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Создайте новый проект VBA.
auto project = System::MakeObject<Aspose::Words::Vba::VbaProject>();
project->set_Name(u"Aspose.Project");
doc->set_VbaProject(project);

// Создайте новый модуль и укажите исходный код макроса.
auto module_ = System::MakeObject<Aspose::Words::Vba::VbaModule>();
module_->set_Name(u"Aspose.Module");
module_->set_Type(Aspose::Words::Vba::VbaModuleType::ProceduralModule);
module_->set_SourceCode(u"New source code");

// Добавьте модуль в проект VBA.
doc->get_VbaProject()->get_Modules()->Add(module_);

doc->Save(get_ArtifactsDir() + u"VbaProject.CreateVBAMacros.docm");
```

## См. также

* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
