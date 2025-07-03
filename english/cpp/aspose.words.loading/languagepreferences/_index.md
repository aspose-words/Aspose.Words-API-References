---
title: Aspose::Words::Loading::LanguagePreferences class
linktitle: LanguagePreferences
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Loading::LanguagePreferences class. Allows to set up language preferences. To learn more, visit the  documentation article in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class


Allows to set up language preferences. To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/) documentation article.

```cpp
class LanguagePreferences : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [AddEditingLanguage](./addeditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Adds additional editing language. |
| [AddEditingLanguages](./addeditinglanguages/)(const System::ArrayPtr\<Aspose::Words::Loading::EditingLanguage\>\&) | Adds additional editing languages. |
| [get_DefaultEditingLanguage](./get_defaulteditinglanguage/)() const | Gets or sets default editing language. The default value is [EnglishUS](../editinglanguage/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LanguagePreferences](./languagepreferences/)() |  |
| [set_DefaultEditingLanguage](./set_defaulteditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Setter for [Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage](./get_defaulteditinglanguage/). |
| static [Type](./type/)() |  |

## Examples



Shows how to apply language preferences when loading a document. 
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->AddEditingLanguage(Aspose::Words::Loading::EditingLanguage::Japanese);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeIdFarEast = doc->get_Styles()->get_DefaultFont()->get_LocaleIdFarEast();
std::cout << (localeIdFarEast == (int32_t)Aspose::Words::Loading::EditingLanguage::Japanese ? System::String(u"The document either has no any FarEast language set in defaults or it was set to Japanese originally.") : System::String(u"The document default FarEast language was set to another than Japanese language originally, so it is not overridden.")) << std::endl;
```

## See Also

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
