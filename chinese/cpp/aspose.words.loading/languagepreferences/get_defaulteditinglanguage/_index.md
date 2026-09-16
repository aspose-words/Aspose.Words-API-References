---
title: "Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage 方法"
linktitle: "get_DefaultEditingLanguage"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage 方法。获取或设置默认编辑语言。默认值在 C++ 中为 EnglishUS。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.loading/languagepreferences/get_defaulteditinglanguage/
---
## LanguagePreferences::get_DefaultEditingLanguage method


获取或设置默认编辑语言。默认值为 [EnglishUS](../../editinglanguage/)。

```cpp
Aspose::Words::Loading::EditingLanguage Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage() const
```


## 示例



展示如何在加载文档时设置默认语言。
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->set_DefaultEditingLanguage(Aspose::Words::Loading::EditingLanguage::Russian);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeId = doc->get_Styles()->get_DefaultFont()->get_LocaleId();
std::cout << (localeId == (int32_t)Aspose::Words::Loading::EditingLanguage::Russian ? System::String(u"The document either has no any language set in defaults or it was set to Russian originally.") : System::String(u"The document default language was set to another than Russian language originally, so it is not overridden.")) << std::endl;
```

## 另见

* Enum [EditingLanguage](../../editinglanguage/)
* Class [LanguagePreferences](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
