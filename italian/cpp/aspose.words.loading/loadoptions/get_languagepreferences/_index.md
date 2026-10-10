---
title: "Aspose::Words::Loading::LoadOptions::get_LanguagePreferences metodo"
linktitle: "get_LanguagePreferences"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::LoadOptions::get_LanguagePreferences metodo. Ottiene le preferenze linguistiche che verranno utilizzate quando il documento viene caricato in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.loading/loadoptions/get_languagepreferences/
---
## LoadOptions::get_LanguagePreferences method


Ottiene le preferenze linguistiche che verranno utilizzate durante il caricamento del documento.

```cpp
System::SharedPtr<Aspose::Words::Loading::LanguagePreferences> Aspose::Words::Loading::LoadOptions::get_LanguagePreferences() const
```


## Esempi



Mostra come applicare le preferenze di lingua durante il caricamento di un documento.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->AddEditingLanguage(Aspose::Words::Loading::EditingLanguage::Japanese);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeIdFarEast = doc->get_Styles()->get_DefaultFont()->get_LocaleIdFarEast();
std::cout << (localeIdFarEast == (int32_t)Aspose::Words::Loading::EditingLanguage::Japanese ? System::String(u"The document either has no any FarEast language set in defaults or it was set to Japanese originally.") : System::String(u"The document default FarEast language was set to another than Japanese language originally, so it is not overridden.")) << std::endl;
```

## Vedi anche

* Class [LanguagePreferences](../../languagepreferences/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
