---
title: "Classe Aspose::Words::Loading::LanguagePreferences"
linktitle: "LanguagePreferences"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Loading::LanguagePreferences. Consente di impostare le preferenze linguistiche. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class


Consente di impostare le preferenze linguistiche. Per saperne di più, visita l'articolo di documentazione [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class LanguagePreferences : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [AddEditingLanguage](./addeditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Aggiunge una lingua di modifica aggiuntiva. |
| [AddEditingLanguages](./addeditinglanguages/)(const System::ArrayPtr\<Aspose::Words::Loading::EditingLanguage\>\&) | Aggiunge lingue di modifica aggiuntive. |
| [get_DefaultEditingLanguage](./get_defaulteditinglanguage/)() const | Ottiene o imposta la lingua di modifica predefinita. Il valore predefinito è [EnglishUS](../editinglanguage/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LanguagePreferences](./languagepreferences/)() |  |
| [set_DefaultEditingLanguage](./set_defaulteditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Impostatore per [Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage](./get_defaulteditinglanguage/). |
| static [Type](./type/)() |  |

## Esempi



Mostra come applicare le preferenze di lingua durante il caricamento di un documento.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->AddEditingLanguage(Aspose::Words::Loading::EditingLanguage::Japanese);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeIdFarEast = doc->get_Styles()->get_DefaultFont()->get_LocaleIdFarEast();
std::cout << (localeIdFarEast == (int32_t)Aspose::Words::Loading::EditingLanguage::Japanese ? System::String(u"The document either has no any FarEast language set in defaults or it was set to Japanese originally.") : System::String(u"The document default FarEast language was set to another than Japanese language originally, so it is not overridden.")) << std::endl;
```

## Vedi anche

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
