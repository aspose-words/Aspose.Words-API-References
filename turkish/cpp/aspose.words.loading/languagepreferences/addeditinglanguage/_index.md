---
title: "Aspose::Words::Loading::LanguagePreferences::AddEditingLanguage metodu"
linktitle: "AddEditingLanguage"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LanguagePreferences::AddEditingLanguage metodu. C++'ta ek düzenleme dili ekler."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences::AddEditingLanguage method


Ek bir düzenleme dili ekler.

```cpp
void Aspose::Words::Loading::LanguagePreferences::AddEditingLanguage(Aspose::Words::Loading::EditingLanguage language)
```


## Örnekler



Bir belge yüklerken dil tercihlerini nasıl uygulayacağınızı gösterir.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->AddEditingLanguage(Aspose::Words::Loading::EditingLanguage::Japanese);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeIdFarEast = doc->get_Styles()->get_DefaultFont()->get_LocaleIdFarEast();
std::cout << (localeIdFarEast == (int32_t)Aspose::Words::Loading::EditingLanguage::Japanese ? System::String(u"The document either has no any FarEast language set in defaults or it was set to Japanese originally.") : System::String(u"The document default FarEast language was set to another than Japanese language originally, so it is not overridden.")) << std::endl;
```

## Ayrıca Bakınız

* Enum [EditingLanguage](../../editinglanguage/)
* Class [LanguagePreferences](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
