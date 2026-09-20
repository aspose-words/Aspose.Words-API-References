---
title: "Aspose::Words::Vba::VbaModule::Clone метод"
linktitle: "Клонировать"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Vba::VbaModule::Clone method. Выполняет копирование VbaModule в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.vba/vbamodule/clone/
---
## VbaModule::Clone method


Выполняет копирование [VbaModule](../).

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModule> Aspose::Words::Vba::VbaModule::Clone()
```


### ReturnValue

Клонированный [VbaModule](../).

## Примеры



Показывает, как глубоко клонировать проект VBA и модуль.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");
auto destDoc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Vba::VbaProject> copyVbaProject = doc->get_VbaProject()->Clone();
destDoc->set_VbaProject(copyVbaProject);

// В целевом документе уже есть модуль с именем "Module1"
// потому что мы клонировали его вместе с проектом. Нам потребуется удалить модуль.
System::SharedPtr<Aspose::Words::Vba::VbaModule> oldVbaModule = destDoc->get_VbaProject()->get_Modules()->idx_get(u"Module1");
System::SharedPtr<Aspose::Words::Vba::VbaModule> copyVbaModule = doc->get_VbaProject()->get_Modules()->idx_get(u"Module1")->Clone();
destDoc->get_VbaProject()->get_Modules()->Remove(oldVbaModule);
destDoc->get_VbaProject()->get_Modules()->Add(copyVbaModule);

destDoc->Save(get_ArtifactsDir() + u"VbaProject.CloneVbaProject.docm");
```

## См. также

* Class [VbaModule](../)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
