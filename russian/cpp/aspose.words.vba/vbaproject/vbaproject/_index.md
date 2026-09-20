---
title: "Конструктор Aspose::Words::Vba::VbaProject::VbaProject"
linktitle: "VbaProject"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор Aspose::Words::Vba::VbaProject::VbaProject. Создает пустой VbaProject в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject::VbaProject constructor


Создает пустой [VbaProject](../).

```cpp
Aspose::Words::Vba::VbaProject::VbaProject()
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

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
