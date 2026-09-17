---
title: "Classe Aspose::Words::Loading::LanguagePreferences"
linktitle: "LanguagePreferences"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::Loading::LanguagePreferences. Permet de configurer les préférences linguistiques. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class


Permet de configurer les préférences de langue. Pour en savoir plus, consultez l'article de documentation [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class LanguagePreferences : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [AddEditingLanguage](./addeditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Ajoute une langue d'édition supplémentaire. |
| [AddEditingLanguages](./addeditinglanguages/)(const System::ArrayPtr\<Aspose::Words::Loading::EditingLanguage\>\&) | Ajoute des langues d'édition supplémentaires. |
| [get_DefaultEditingLanguage](./get_defaulteditinglanguage/)() const | Obtient ou définit la langue d'édition par défaut. La valeur par défaut est [EnglishUS](../editinglanguage/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LanguagePreferences](./languagepreferences/)() |  |
| [set_DefaultEditingLanguage](./set_defaulteditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Définisseur pour [Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage](./get_defaulteditinglanguage/). |
| static [Type](./type/)() |  |

## Exemples



Montre comment appliquer les préférences de langue lors du chargement d'un document.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->AddEditingLanguage(Aspose::Words::Loading::EditingLanguage::Japanese);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeIdFarEast = doc->get_Styles()->get_DefaultFont()->get_LocaleIdFarEast();
std::cout << (localeIdFarEast == (int32_t)Aspose::Words::Loading::EditingLanguage::Japanese ? System::String(u"The document either has no any FarEast language set in defaults or it was set to Japanese originally.") : System::String(u"The document default FarEast language was set to another than Japanese language originally, so it is not overridden.")) << std::endl;
```

## Voir aussi

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
