---
title: "الفئة Aspose::Words::Loading::LanguagePreferences"
linktitle: "تفضيلات اللغة"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Loading::LanguagePreferences. يسمح بتعيين تفضيلات اللغة. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class


يسمح بإعداد تفضيلات اللغة. لمزيد من المعلومات، قم بزيارة مقالة الوثائق [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class LanguagePreferences : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [AddEditingLanguage](./addeditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | يضيف لغة تحرير إضافية. |
| [AddEditingLanguages](./addeditinglanguages/)(const System::ArrayPtr\<Aspose::Words::Loading::EditingLanguage\>\&) | يضيف لغات تحرير إضافية. |
| [get_DefaultEditingLanguage](./get_defaulteditinglanguage/)() const | يحصل أو يعيّن لغة التحرير الافتراضية. القيمة الافتراضية هي [EnglishUS](../editinglanguage/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LanguagePreferences](./languagepreferences/)() |  |
| [set_DefaultEditingLanguage](./set_defaulteditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | مُعيّن لـ [Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage](./get_defaulteditinglanguage/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
