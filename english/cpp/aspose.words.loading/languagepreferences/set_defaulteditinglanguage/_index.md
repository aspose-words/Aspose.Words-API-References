---
title: Aspose::Words::Loading::LanguagePreferences::set_DefaultEditingLanguage method
linktitle: set_DefaultEditingLanguage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LanguagePreferences::set_DefaultEditingLanguage method. Sets default editing language.The default value is EnglishUS in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.loading/languagepreferences/set_defaulteditinglanguage/
---
## LanguagePreferences::set_DefaultEditingLanguage method


Sets default editing language.

The default value is [EnglishUS](../../editinglanguage/).

```cpp
void Aspose::Words::Loading::LanguagePreferences::set_DefaultEditingLanguage(Aspose::Words::Loading::EditingLanguage value)
```

## Examples


Shows how set a default language when loading a document.

```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->set_DefaultEditingLanguage(EditingLanguage::Russian);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeId = doc->get_Styles()->get_DefaultFont()->get_LocaleId();
std::cout << (localeId == (int32_t)EditingLanguage::Russian ? System::String(u"The document either has no any language set in defaults or it was set to Russian originally.") : System::String(u"The document default language was set to another than Russian language originally, so it is not overridden.")) << std::endl;
```
## See Also

* Class [LanguagePreferences](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
