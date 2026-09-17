---
title: "Aspose::Words::Vba::VbaModuleCollection::Add méthode"
linktitle: "Add"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Vba::VbaModuleCollection::Add méthode. Ajoute un module à la collection en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.vba/vbamodulecollection/add/
---
## VbaModuleCollection::Add method


Ajoute un module à la collection.

```cpp
void Aspose::Words::Vba::VbaModuleCollection::Add(const System::SharedPtr<Aspose::Words::Vba::VbaModule> &vbaModule)
```


## Exemples



Montre comment créer un projet VBA à l'aide de macros.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Créez un nouveau projet VBA.
auto project = System::MakeObject<Aspose::Words::Vba::VbaProject>();
project->set_Name(u"Aspose.Project");
doc->set_VbaProject(project);

// Créez un nouveau module et spécifiez le code source d'une macro.
auto module_ = System::MakeObject<Aspose::Words::Vba::VbaModule>();
module_->set_Name(u"Aspose.Module");
module_->set_Type(Aspose::Words::Vba::VbaModuleType::ProceduralModule);
module_->set_SourceCode(u"New source code");

// Ajoutez le module au projet VBA.
doc->get_VbaProject()->get_Modules()->Add(module_);

doc->Save(get_ArtifactsDir() + u"VbaProject.CreateVBAMacros.docm");
```

## Voir aussi

* Class [VbaModule](../../vbamodule/)
* Class [VbaModuleCollection](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
