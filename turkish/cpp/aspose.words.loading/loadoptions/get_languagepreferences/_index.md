---
title: "Aspose::Words::Loading::LoadOptions::get_LanguagePreferences yöntemi"
linktitle: "get_LanguagePreferences"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::get_LanguagePreferences yöntemi. Belge yüklendiğinde kullanılacak dil tercihlerini C++'ta alır."
type: docs
weight: 9000
url: /tr/cpp/aspose.words.loading/loadoptions/get_languagepreferences/
---
## LoadOptions::get_LanguagePreferences method


Belge yüklendiğinde kullanılacak dil tercihlerini alır.

```cpp
System::SharedPtr<Aspose::Words::Loading::LanguagePreferences> Aspose::Words::Loading::LoadOptions::get_LanguagePreferences() const
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

* Class [LanguagePreferences](../../languagepreferences/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
