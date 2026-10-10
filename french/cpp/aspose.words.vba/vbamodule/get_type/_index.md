---
title: "Aspose::Words::Vba::VbaModule::get_Type méthode"
linktitle: "get_Type"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Vba::VbaModule::get_Type méthode. Spécifie si le module est un module procédural, un module de document, un module de classe ou un module de conception en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.vba/vbamodule/get_type/
---
## VbaModule::get_Type method


Spécifie si le module est un module procédural, un module de document, un module de classe ou un module de concepteur.

```cpp
Aspose::Words::Vba::VbaModuleType Aspose::Words::Vba::VbaModule::get_Type() const
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

* Enum [VbaModuleType](../../vbamoduletype/)
* Class [VbaModule](../)
* Namespace [Aspose::Words::Vba](../../)
* Library [Aspose.Words for C++](../../../)
