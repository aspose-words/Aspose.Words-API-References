---
title: "Aspose::Words::Vba::VbaModule class"
linktitle: "VbaModule"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Vba::VbaModule class. Fournit un accès au module du projet VBA. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.vba/vbamodule/
---
## VbaModule class


Fournit l'accès au module de projet VBA. Pour en savoir plus, consultez l'article de documentation [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaModule : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clone](./clone/)() | Effectue une copie du [VbaModule](./). |
| [get_Name](./get_name/)() const | Obtient ou définit le nom du module du projet VBA. |
| [get_SourceCode](./get_sourcecode/)() const | Obtient ou définit le code source du module du projet VBA. |
| [get_Type](./get_type/)() const | Spécifie si le module est un module procédural, un module de document, un module de classe ou un module de concepteur. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Name](./set_name/)(const System::String\&) | Mutateur pour [Aspose::Words::Vba::VbaModule::get_Name](./get_name/). |
| [set_SourceCode](./set_sourcecode/)(const System::String\&) | Mutateur pour [Aspose::Words::Vba::VbaModule::get_SourceCode](./get_sourcecode/). |
| [set_Type](./set_type/)(Aspose::Words::Vba::VbaModuleType) | Mutateur pour [Aspose::Words::Vba::VbaModule::get_Type](./get_type/). |
| static [Type](./type/)() |  |
| [VbaModule](./vbamodule/)() | Crée un module vide. |

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

* Namespace [Aspose::Words::Vba](../)
* Library [Aspose.Words for C++](../../)
