---
title: "Aspose::Words::Loading::LanguagePreferences 类"
linktitle: "LanguagePreferences"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::LanguagePreferences 类。允许设置语言首选项。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class


允许设置语言首选项。欲了解更多，请访问[Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/)文档文章。

```cpp
class LanguagePreferences : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [AddEditingLanguage](./addeditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | 添加额外的编辑语言。 |
| [AddEditingLanguages](./addeditinglanguages/)(const System::ArrayPtr\<Aspose::Words::Loading::EditingLanguage\>\&) | 添加额外的编辑语言。 |
| [get_DefaultEditingLanguage](./get_defaulteditinglanguage/)() const | 获取或设置默认编辑语言。默认值是 [EnglishUS](../editinglanguage/)。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LanguagePreferences](./languagepreferences/)() |  |
| [set_DefaultEditingLanguage](./set_defaulteditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | 用于设置 [Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage](./get_defaulteditinglanguage/) 的 setter。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
