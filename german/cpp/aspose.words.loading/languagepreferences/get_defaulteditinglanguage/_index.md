---
title: "Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage method"
linktitle: "get_DefaultEditingLanguage"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage method. Ruft die Standardsprache für die Bearbeitung ab oder legt sie fest. Der Standardwert ist EnglishUS in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.loading/languagepreferences/get_defaulteditinglanguage/
---
## LanguagePreferences::get_DefaultEditingLanguage method


Ruft die Standardsprache für die Bearbeitung ab oder legt sie fest. Der Standardwert ist [EnglishUS](../../editinglanguage/).

```cpp
Aspose::Words::Loading::EditingLanguage Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage() const
```


## Beispiele



Zeigt, wie man beim Laden eines Dokuments eine Standardsprache festlegt.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->set_DefaultEditingLanguage(Aspose::Words::Loading::EditingLanguage::Russian);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeId = doc->get_Styles()->get_DefaultFont()->get_LocaleId();
std::cout << (localeId == (int32_t)Aspose::Words::Loading::EditingLanguage::Russian ? System::String(u"The document either has no any language set in defaults or it was set to Russian originally.") : System::String(u"The document default language was set to another than Russian language originally, so it is not overridden.")) << std::endl;
```

## Siehe auch

* Enum [EditingLanguage](../../editinglanguage/)
* Class [LanguagePreferences](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
