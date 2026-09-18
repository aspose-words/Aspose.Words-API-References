---
title: "Aspose::Words::Loading::LanguagePreferences Klasse"
linktitle: "LanguagePreferences"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::LanguagePreferences Klasse. Ermöglicht das Festlegen von Spracheinstellungen. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 4000
url: /de/cpp/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class


Ermöglicht das Festlegen von Spracheinstellungen. Weitere Informationen finden Sie im Dokumentationsartikel [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class LanguagePreferences : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [AddEditingLanguage](./addeditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Fügt eine zusätzliche Bearbeitungssprache hinzu. |
| [AddEditingLanguages](./addeditinglanguages/)(const System::ArrayPtr\<Aspose::Words::Loading::EditingLanguage\>\&) | Fügt zusätzliche Bearbeitungssprachen hinzu. |
| [get_DefaultEditingLanguage](./get_defaulteditinglanguage/)() const | Liest oder setzt die Standardsprache für die Bearbeitung. Der Standardwert ist [EnglishUS](../editinglanguage/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LanguagePreferences](./languagepreferences/)() |  |
| [set_DefaultEditingLanguage](./set_defaulteditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Setter für [Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage](./get_defaulteditinglanguage/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie Sprachpräferenzen beim Laden eines Dokuments angewendet werden.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->AddEditingLanguage(Aspose::Words::Loading::EditingLanguage::Japanese);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeIdFarEast = doc->get_Styles()->get_DefaultFont()->get_LocaleIdFarEast();
std::cout << (localeIdFarEast == (int32_t)Aspose::Words::Loading::EditingLanguage::Japanese ? System::String(u"The document either has no any FarEast language set in defaults or it was set to Japanese originally.") : System::String(u"The document default FarEast language was set to another than Japanese language originally, so it is not overridden.")) << std::endl;
```

## Siehe auch

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
