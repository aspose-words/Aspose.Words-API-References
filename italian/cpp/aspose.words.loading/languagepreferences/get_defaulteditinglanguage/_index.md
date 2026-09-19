---
title: "Metodo get_DefaultEditingLanguage di Aspose::Words::Loading::LanguagePreferences"
linktitle: "get_DefaultEditingLanguage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_DefaultEditingLanguage di Aspose::Words::Loading::LanguagePreferences. Ottiene o imposta la lingua di modifica predefinita. Il valore predefinito è EnglishUS in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.loading/languagepreferences/get_defaulteditinglanguage/
---
## LanguagePreferences::get_DefaultEditingLanguage method


Ottiene o imposta la lingua di modifica predefinita. Il valore predefinito è [EnglishUS](../../editinglanguage/).

```cpp
Aspose::Words::Loading::EditingLanguage Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage() const
```


## Esempi



Mostra come impostare una lingua predefinita durante il caricamento di un documento.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->set_DefaultEditingLanguage(Aspose::Words::Loading::EditingLanguage::Russian);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeId = doc->get_Styles()->get_DefaultFont()->get_LocaleId();
std::cout << (localeId == (int32_t)Aspose::Words::Loading::EditingLanguage::Russian ? System::String(u"The document either has no any language set in defaults or it was set to Russian originally.") : System::String(u"The document default language was set to another than Russian language originally, so it is not overridden.")) << std::endl;
```

## Vedi anche

* Enum [EditingLanguage](../../editinglanguage/)
* Class [LanguagePreferences](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
