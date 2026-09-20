---
title: "Aspose::Words::Vba::VbaProject::get_IsSigned метод"
linktitle: "get_IsSigned"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Vba::VbaProject::get_IsSigned метод. Показывает, подписан ли VbaProject или нет в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.vba/vbaproject/get_issigned/
---
## VbaProject::get_IsSigned method


Показывает, подписан ли [VbaProject](../) или нет.

```cpp
bool Aspose::Words::Vba::VbaProject::get_IsSigned()
```


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

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
