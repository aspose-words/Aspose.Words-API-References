---
title: "طريقة Aspose::Words::Loading::LanguagePreferences::AddEditingLanguage"
linktitle: "AddEditingLanguage"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Loading::LanguagePreferences::AddEditingLanguage. يضيف لغة تحرير إضافية في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences::AddEditingLanguage method


يضيف لغة تحرير إضافية.

```cpp
void Aspose::Words::Loading::LanguagePreferences::AddEditingLanguage(Aspose::Words::Loading::EditingLanguage language)
```


## أمثلة



يوضح كيفية تطبيق تفضيلات اللغة عند تحميل مستند.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->AddEditingLanguage(Aspose::Words::Loading::EditingLanguage::Japanese);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeIdFarEast = doc->get_Styles()->get_DefaultFont()->get_LocaleIdFarEast();
std::cout << (localeIdFarEast == (int32_t)Aspose::Words::Loading::EditingLanguage::Japanese ? System::String(u"The document either has no any FarEast language set in defaults or it was set to Japanese originally.") : System::String(u"The document default FarEast language was set to another than Japanese language originally, so it is not overridden.")) << std::endl;
```

## انظر أيضًا

* Enum [EditingLanguage](../../editinglanguage/)
* Class [LanguagePreferences](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
