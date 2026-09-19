---
title: "Metodo AddEditingLanguage di Aspose::Words::Loading::LanguagePreferences"
linktitle: "AddEditingLanguage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo AddEditingLanguage di Aspose::Words::Loading::LanguagePreferences. Aggiunge una lingua di modifica aggiuntiva in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences::AddEditingLanguage method


Aggiunge una lingua di modifica aggiuntiva.

```cpp
void Aspose::Words::Loading::LanguagePreferences::AddEditingLanguage(Aspose::Words::Loading::EditingLanguage language)
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

* Enum [EditingLanguage](../../editinglanguage/)
* Class [LanguagePreferences](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
