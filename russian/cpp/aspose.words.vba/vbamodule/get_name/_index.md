---
title: "Aspose::Words::Vba::VbaModule::get_Name метод"
linktitle: "get_Name"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Vba::VbaModule::get_Name метод. Получает или задает имя модуля проекта VBA в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.vba/vbamodule/get_name/
---
## VbaModule::get_Name method


Получает или задаёт имя модуля проекта VBA.

```cpp
System::String Aspose::Words::Vba::VbaModule::get_Name() const
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
