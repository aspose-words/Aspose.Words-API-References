---
title: "méthode Aspose::Words::Loading::LoadOptions::get_LanguagePreferences"
linktitle: "get_LanguagePreferences"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "méthode Aspose::Words::Loading::LoadOptions::get_LanguagePreferences. Obtient les préférences linguistiques qui seront utilisées lors du chargement du document en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.loading/loadoptions/get_languagepreferences/
---
## LoadOptions::get_LanguagePreferences method


Obtient les préférences de langue qui seront utilisées lors du chargement du document.

```cpp
System::SharedPtr<Aspose::Words::Loading::LanguagePreferences> Aspose::Words::Loading::LoadOptions::get_LanguagePreferences() const
```


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

* Class [LanguagePreferences](../../languagepreferences/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
