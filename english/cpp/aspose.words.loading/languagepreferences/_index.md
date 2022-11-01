---
title: LanguagePreferences
second_title: Aspose.Words for C++ API Reference
description: Allows to set up language preferences.
type: docs
weight: 40
url: /cpp/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class


Allows to set up language preferences.

```cpp
class LanguagePreferences : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [AddEditingLanguage](./addeditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Adds additional editing language. |
| [AddEditingLanguages](./addeditinglanguages/)(const System::ArrayPtr\<Aspose::Words::Loading::EditingLanguage\>\&) | Adds additional editing languages. |
| [get_DefaultEditingLanguage](./get_defaulteditinglanguage/)() const | Gets or sets default editing language. The default value is **EnglishUS**. |
| [LanguagePreferences](./languagepreferences/)() |  |
| [set_DefaultEditingLanguage](./set_defaulteditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Setter for [Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage](./get_defaulteditinglanguage/). |

## Examples




Shows how to apply language preferences when loading a document. 
```cpp
auto loadOptions = MakeObject<LoadOptions>();
loadOptions->get_LanguagePreferences()->AddEditingLanguage(EditingLanguage::Japanese);

auto doc = MakeObject<Document>(MyDir + u"No default editing language.docx", loadOptions);

int localeIdFarEast = doc->get_Styles()->get_DefaultFont()->get_LocaleIdFarEast();
std::cout << (localeIdFarEast == (int)EditingLanguage::Japanese
                  ? String(u"The document either has no any FarEast language set in defaults or it was set to Japanese originally.")
                  : String(u"The document default FarEast language was set to another than Japanese language originally, so it is not overridden."))
          << std::endl;
```

