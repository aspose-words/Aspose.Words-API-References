---
title: "Aspose::Words::Loading::LanguagePreferences sınıfı"
linktitle: "LanguagePreferences"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LanguagePreferences sınıfı. Dil tercihlerini ayarlamayı sağlar. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class


Dil tercihlerini ayarlamaya olanak tanır. Daha fazla bilgi için, [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) dokümantasyon makalesini ziyaret edin.

```cpp
class LanguagePreferences : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [AddEditingLanguage](./addeditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Ek bir düzenleme dili ekler. |
| [AddEditingLanguages](./addeditinglanguages/)(const System::ArrayPtr\<Aspose::Words::Loading::EditingLanguage\>\&) | Ek düzenleme dilleri ekler. |
| [get_DefaultEditingLanguage](./get_defaulteditinglanguage/)() const | Varsayılan düzenleme dilini alır veya ayarlar. Varsayılan değer [EnglishUS](../editinglanguage/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LanguagePreferences](./languagepreferences/)() |  |
| [set_DefaultEditingLanguage](./set_defaulteditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | [Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage](./get_defaulteditinglanguage/) için ayarlayıcı. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
