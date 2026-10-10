---
title: "Aspose::Words::Vba::VbaProject classe"
linktitle: "VbaProject"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Vba::VbaProject classe. Fournit l'accès aux informations du projet VBA. Un projet VBA dans le document est défini comme une collection de modules VBA. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.vba/vbaproject/
---
## VbaProject class


Fournit l'accès aux informations du projet VBA. Un projet VBA dans le document est défini comme une collection de modules VBA. Pour en savoir plus, consultez l'article de documentation [Working with VBA Macros](https://docs.aspose.com/words/cpp/working-with-vba-macros/).

```cpp
class VbaProject : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Clone](./clone/)() | Effectue une copie du [VbaProject](./). |
| [get_CodePage](./get_codepage/)() const | Obtient ou définit la page de code du projet VBA. |
| [get_IsProtected](./get_isprotected/)() | Indique si le [VbaProject](./) est protégé par mot de passe. |
| [get_IsSigned](./get_issigned/)() | Indique si le [VbaProject](./) est signé ou non. |
| [get_Modules](./get_modules/)() | Renvoie la collection des modules du projet VBA. |
| [get_Name](./get_name/)() const | Obtient ou définit le nom du projet VBA. |
| [get_References](./get_references/)() | Obtient une collection de références du projet VBA. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CodePage](./set_codepage/)(int32_t) | Mutateur pour [Aspose::Words::Vba::VbaProject::get_CodePage](./get_codepage/). |
| [set_Name](./set_name/)(const System::String\&) | Mutateur pour [Aspose::Words::Vba::VbaProject::get_Name](./get_name/). |
| static [Type](./type/)() |  |
| [VbaProject](./vbaproject/)() | Crée un [VbaProject](./) vierge. |

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
