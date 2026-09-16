---
title: "Aspose::Words::Loading::LoadOptions::get_LanguagePreferences 方法"
linktitle: "get_LanguagePreferences"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LoadOptions::get_LanguagePreferences 方法。获取在 C++ 中加载文档时将使用的语言首选项。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.loading/loadoptions/get_languagepreferences/
---
## LoadOptions::get_LanguagePreferences method


获取在文档加载时将使用的语言首选项。

```cpp
System::SharedPtr<Aspose::Words::Loading::LanguagePreferences> Aspose::Words::Loading::LoadOptions::get_LanguagePreferences() const
```


## 示例



展示如何在加载文档时应用语言首选项。
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->AddEditingLanguage(Aspose::Words::Loading::EditingLanguage::Japanese);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeIdFarEast = doc->get_Styles()->get_DefaultFont()->get_LocaleIdFarEast();
std::cout << (localeIdFarEast == (int32_t)Aspose::Words::Loading::EditingLanguage::Japanese ? System::String(u"The document either has no any FarEast language set in defaults or it was set to Japanese originally.") : System::String(u"The document default FarEast language was set to another than Japanese language originally, so it is not overridden.")) << std::endl;
```

## 另见

* Class [LanguagePreferences](../../languagepreferences/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
