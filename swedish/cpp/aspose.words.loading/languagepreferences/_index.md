---
title: "Aspose::Words::Loading::LanguagePreferences klass"
linktitle: "LanguagePreferences"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LanguagePreferences-klass. Tillåter att ställa in språkpreferenser. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class


Gör det möjligt att ställa in språkpreferenser. För att lära dig mer, besök dokumentationsartikeln [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class LanguagePreferences : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [AddEditingLanguage](./addeditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Lägger till ytterligare redigeringsspråk. |
| [AddEditingLanguages](./addeditinglanguages/)(const System::ArrayPtr\<Aspose::Words::Loading::EditingLanguage\>\&) | Lägger till ytterligare redigeringsspråk. |
| [get_DefaultEditingLanguage](./get_defaulteditinglanguage/)() const | Hämtar eller anger standardredigeringsspråk. Standardvärdet är [EnglishUS](../editinglanguage/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LanguagePreferences](./languagepreferences/)() |  |
| [set_DefaultEditingLanguage](./set_defaulteditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Sättare för [Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage](./get_defaulteditinglanguage/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man tillämpar språkpreferenser när man laddar ett dokument.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->AddEditingLanguage(Aspose::Words::Loading::EditingLanguage::Japanese);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeIdFarEast = doc->get_Styles()->get_DefaultFont()->get_LocaleIdFarEast();
std::cout << (localeIdFarEast == (int32_t)Aspose::Words::Loading::EditingLanguage::Japanese ? System::String(u"The document either has no any FarEast language set in defaults or it was set to Japanese originally.") : System::String(u"The document default FarEast language was set to another than Japanese language originally, so it is not overridden.")) << std::endl;
```

## Se även

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
