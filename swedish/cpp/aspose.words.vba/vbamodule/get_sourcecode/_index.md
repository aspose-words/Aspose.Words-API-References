---
title: "Aspose::Words::Vba::VbaModule::get_SourceCode-metod"
linktitle: "get_SourceCode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Vba::VbaModule::get_SourceCode-metod. Hämtar eller anger källkoden för VBA-projektmodulen i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.vba/vbamodule/get_sourcecode/
---
## VbaModule::get_SourceCode method


Hämtar eller anger VBA-projektmodulens källkod.

```cpp
System::String Aspose::Words::Vba::VbaModule::get_SourceCode() const
```


## Exempel



Visar hur man får åtkomst till information om ett dokuments VBA-projekt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");

// Ett VBA-projekt innehåller en samling av VBA-moduler.
System::SharedPtr<Aspose::Words::Vba::VbaProject> vbaProject = doc->get_VbaProject();
std::cout << (vbaProject->get_IsSigned() ? System::String::Format(u"Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count()) : System::String::Format(u"Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count())) << std::endl;

System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> vbaModules = doc->get_VbaProject()->get_Modules();

ASSERT_EQ(vbaModules->LINQ_Count(), 3);

for (auto&& module_ : vbaModules)
{
    std::cout << System::String::Format(u"Module name: {0};\nModule code:\n{1}\n", module_->get_Name(), module_->get_SourceCode()) << std::endl;
}

// Ställ in ny källkod för VBA-modulen. Du kan komma åt VBA-moduler i samlingen antingen via index eller via namn.
vbaModules->idx_get(0)->set_SourceCode(u"Your VBA code...");
vbaModules->idx_get(u"Module1")->set_SourceCode(u"Your VBA code...");

// Ta bort en modul från samlingen.
vbaModules->Remove(vbaModules->idx_get(2));
```


Visar hur man skapar ett VBA-projekt med makron.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Skapa ett nytt VBA-projekt.
auto project = System::MakeObject<Aspose::Words::Vba::VbaProject>();
project->set_Name(u"Aspose.Project");
doc->set_VbaProject(project);

// Skapa en ny modul och ange makrokällkod.
auto module_ = System::MakeObject<Aspose::Words::Vba::VbaModule>();
module_->set_Name(u"Aspose.Module");
module_->set_Type(Aspose::Words::Vba::VbaModuleType::ProceduralModule);
module_->set_SourceCode(u"New source code");

// Lägg till modulen i VBA-projektet.
doc->get_VbaProject()->get_Modules()->Add(module_);

doc->Save(get_ArtifactsDir() + u"VbaProject.CreateVBAMacros.docm");
```

## Se även

* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
