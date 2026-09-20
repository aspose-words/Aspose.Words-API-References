---
title: "Метод Aspose::Words::Vba::VbaModuleCollection::Remove"
linktitle: "Remove"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Vba::VbaModuleCollection::Remove. Удаляет указанный модуль из коллекции в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.vba/vbamodulecollection/remove/
---
## VbaModuleCollection::Remove method


Удаляет указанный модуль из коллекции.

```cpp
void Aspose::Words::Vba::VbaModuleCollection::Remove(const System::SharedPtr<Aspose::Words::Vba::VbaModule> &module_)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| module_ | const System::SharedPtr\<Aspose::Words::Vba::VbaModule\>\& | Модуль для удаления. |

## Примеры



Показывает, как получить доступ к информации о VBA‑проекте документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");

// Проект VBA содержит коллекцию модулей VBA.
System::SharedPtr<Aspose::Words::Vba::VbaProject> vbaProject = doc->get_VbaProject();
std::cout << (vbaProject->get_IsSigned() ? System::String::Format(u"Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count()) : System::String::Format(u"Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count())) << std::endl;

System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> vbaModules = doc->get_VbaProject()->get_Modules();

ASSERT_EQ(vbaModules->LINQ_Count(), 3);

for (auto&& module_ : vbaModules)
{
    std::cout << System::String::Format(u"Module name: {0};\nModule code:\n{1}\n", module_->get_Name(), module_->get_SourceCode()) << std::endl;
}

// Установите новый исходный код для модуля VBA. Вы можете получить доступ к модулям VBA в коллекции либо по индексу, либо по имени.
vbaModules->idx_get(0)->set_SourceCode(u"Your VBA code...");
vbaModules->idx_get(u"Module1")->set_SourceCode(u"Your VBA code...");

// Удалите модуль из коллекции.
vbaModules->Remove(vbaModules->idx_get(2));
```

## См. также

* Class [VbaModule](../../vbamodule/)
* Class [VbaModuleCollection](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
