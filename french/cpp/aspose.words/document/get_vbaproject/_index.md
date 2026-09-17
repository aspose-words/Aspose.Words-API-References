---
title: "Aspose::Words::Document::get_VbaProject méthode"
linktitle: "get_VbaProject"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Document::get_VbaProject méthode. Obtient ou définit un VbaProject en C++."
type: docs
weight: 56000
url: /fr/cpp/aspose.words/document/get_vbaproject/
---
## Document::get_VbaProject method


Obtient ou définit un [VbaProject](./).

```cpp
System::SharedPtr<Aspose::Words::Vba::VbaProject> Aspose::Words::Document::get_VbaProject() const
```


## Exemples



Montre comment accéder aux informations du projet VBA d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VBA project.docm");

// Un projet VBA contient une collection de modules VBA.
System::SharedPtr<Aspose::Words::Vba::VbaProject> vbaProject = doc->get_VbaProject();
std::cout << (vbaProject->get_IsSigned() ? System::String::Format(u"Project name: {0} signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count()) : System::String::Format(u"Project name: {0} not signed; Project code page: {1}; Modules count: {2}\n", vbaProject->get_Name(), vbaProject->get_CodePage(), vbaProject->get_Modules()->LINQ_Count())) << std::endl;

System::SharedPtr<Aspose::Words::Vba::VbaModuleCollection> vbaModules = doc->get_VbaProject()->get_Modules();

ASSERT_EQ(vbaModules->LINQ_Count(), 3);

for (auto&& module_ : vbaModules)
{
    std::cout << System::String::Format(u"Module name: {0};\nModule code:\n{1}\n", module_->get_Name(), module_->get_SourceCode()) << std::endl;
}

// Définissez un nouveau code source pour le module VBA. Vous pouvez accéder aux modules VBA dans la collection soit par indice, soit par nom.
vbaModules->idx_get(0)->set_SourceCode(u"Your VBA code...");
vbaModules->idx_get(u"Module1")->set_SourceCode(u"Your VBA code...");

// Supprimez un module de la collection.
vbaModules->Remove(vbaModules->idx_get(2));
```

## Voir aussi

* Class [VbaProject](../../../aspose.words.vba/vbaproject/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
