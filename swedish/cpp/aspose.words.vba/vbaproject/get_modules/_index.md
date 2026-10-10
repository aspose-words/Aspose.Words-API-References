---
title: "Aspose::Words::Vba::VbaProject::get_Modules‑metod"
linktitle: "get_Modules"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Vba::VbaProject::get_Modules‑metod. Returnerar en samling av VBA‑projektmoduler i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.vba/vbaproject/get_modules/
---
## VbaProject::get_Modules method


Returnerar en samling av VBA-projektmoduler.

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> Aspose::Words::Vba::VbaProject::get_Modules()
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

## Se även

* Class [VbaModuleCollection](../../vbamodulecollection/)
* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
