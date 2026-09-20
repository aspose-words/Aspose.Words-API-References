---
title: "Aspose::Words::Vba::VbaModule class"
linktitle: "VbaModule"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Vba::VbaModule. Предоставляет доступ к модулю проекта VBA. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.vba/vbamodule/
---
## VbaModule class


Обеспечивает доступ к модулю проекта VBA. Чтобы узнать больше, посетите статью документации [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaModule : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clone](./clone/)() | Выполняет копирование [VbaModule](./). |
| [get_Name](./get_name/)() const | Получает или задаёт имя модуля проекта VBA. |
| [get_SourceCode](./get_sourcecode/)() const | Получает или задаёт исходный код модуля проекта VBA. |
| [get_Type](./get_type/)() const | Указывает, является ли модуль процедурным, документным, классным или дизайнерским. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Name](./set_name/)(const System::String\&) | Сеттер для [Aspose::Words::Vba::VbaModule::get_Name](./get_name/). |
| [set_SourceCode](./set_sourcecode/)(const System::String\&) | Сеттер для [Aspose::Words::Vba::VbaModule::get_SourceCode](./get_sourcecode/). |
| [set_Type](./set_type/)(Aspose::Words::Vba::VbaModuleType) | Сеттер для [Aspose::Words::Vba::VbaModule::get_Type](./get_type/). |
| static [Type](./type/)() |  |
| [VbaModule](./vbamodule/)() | Создаёт пустой модуль. |

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

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
