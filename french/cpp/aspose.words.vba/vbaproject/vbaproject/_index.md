---
title: "Aspose::Words::Vba::VbaProject::VbaProject constructeur"
linktitle: "VbaProject"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Vba::VbaProject::VbaProject constructeur. Crée un VbaProject vierge en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.vba/vbaproject/vbaproject/
---
## VbaProject::VbaProject constructor


Crée un [VbaProject](../) vierge.

```cpp
Aspose::Words::Vba::VbaProject::VbaProject()
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

* Class [VbaProject](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
