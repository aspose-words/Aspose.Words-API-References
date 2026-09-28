---
title: "Aspose::Words::Vba::VbaProject class"
linktitle: "VbaProject"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Vba::VbaProject класс. Предоставляет доступ к информации о VBA‑проекте. VBA‑проект внутри документа определяется как набор VBA‑модулей. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.vba/vbaproject/
---
## VbaProject class


Обеспечивает доступ к информации о проекте VBA. Проект VBA в документе определяется как коллекция модулей VBA. Чтобы узнать больше, посетите статью документации [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaProject : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clone](./clone/)() | Выполняет копирование [VbaProject](./). |
| [get_CodePage](./get_codepage/)() const | Получает или задает кодовую страницу VBA‑проекта. |
| [get_IsProtected](./get_isprotected/)() | Показывает, защищён ли [VbaProject](./) паролем. |
| [get_IsSigned](./get_issigned/)() | Показывает, подписан ли [VbaProject](./) или нет. |
| [get_Modules](./get_modules/)() | Возвращает коллекцию модулей VBA‑проекта. |
| [get_Name](./get_name/)() const | Получает или задает имя VBA‑проекта. |
| [get_References](./get_references/)() | Получает коллекцию ссылок VBA‑проекта. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CodePage](./set_codepage/)(int32_t) | Сеттер для [Aspose::Words::Vba::VbaProject::get_CodePage](./get_codepage/). |
| [set_Name](./set_name/)(const System::String\&) | Сеттер для [Aspose::Words::Vba::VbaProject::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [VbaProject](./vbaproject/)() | Создаёт пустой [VbaProject](./). |

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
