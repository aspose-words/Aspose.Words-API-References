---
title: "Aspose::Words::Vba::VbaModuleType enum"
linktitle: "VbaModuleType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Vba::VbaModuleType enum. Spécifie le type d'un modèle dans un projet VBA en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.vba/vbamoduletype/
---
## VbaModuleType enum


Spécifie le type d'un modèle dans un projet VBA.

```cpp
enum class VbaModuleType
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| DocumentModule | 0 | Un type d'élément de projet VBA qui spécifie un module pour les macros intégrées et les opérations d'accès programmatique associées à un document. |
| ProceduralModule | 1 | Une collection de sous‑routines et de fonctions. |
| ClassModule | 2 | Un module qui contient la définition d'un nouvel objet. Chaque instance d'une classe crée un nouvel objet, et les procédures définies dans le module deviennent des propriétés et des méthodes de l'objet. |
| DesignerModule | 3 | Un module VBA qui étend les méthodes et propriétés d'un contrôle ActiveX enregistré dans le projet. |


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

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
