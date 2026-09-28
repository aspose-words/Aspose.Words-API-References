---
title: "Aspose::Words::Vba::VbaModuleType перечисление"
linktitle: "VbaModuleType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Vba::VbaModuleType перечисление. Указывает тип модели в проекте VBA в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enum


Указывает тип модели в проекте VBA.

```cpp
enum class VbaModuleType
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| DocumentModule | 0 | Тип элемента проекта VBA, который указывает модуль для встроенных макросов и операций программного доступа, связанных с документом. |
| ProceduralModule | 1 | Коллекция подпрограмм и функций. |
| ClassModule | 2 | Модуль, содержащий определение нового объекта. Каждый экземпляр класса создает новый объект, а процедуры, определённые в модуле, становятся свойствами и методами объекта. |
| DesignerModule | 3 | Модуль VBA, расширяющий методы и свойства ActiveX‑контрола, зарегистрированного в проекте. |


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

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
