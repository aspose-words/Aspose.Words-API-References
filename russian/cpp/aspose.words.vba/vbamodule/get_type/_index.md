---
title: "Aspose::Words::Vba::VbaModule::get_Type метод"
linktitle: "get_Type"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Vba::VbaModule::get_Type метод. Указывает, является ли модуль процедурным модулем, модулем документа, модулем класса или модулем дизайнера в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.vba/vbamodule/get_type/
---
## VbaModule::get_Type method


Указывает, является ли модуль процедурным, документным, классным или дизайнерским.

```cpp
Aspose::Words::Vba::VbaModuleType Aspose::Words::Vba::VbaModule::get_Type() const
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

* Enum [VbaModuleType](../../vbamoduletype/)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
