---
title: "Aspose::Words::Loading::LanguagePreferences класс"
linktitle: "LanguagePreferences"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Loading::LanguagePreferences. Позволяет задавать языковые предпочтения. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class


Позволяет задавать языковые предпочтения. Чтобы узнать больше, посетите статью документации [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class LanguagePreferences : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [AddEditingLanguage](./addeditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Добавляет дополнительный язык редактирования. |
| [AddEditingLanguages](./addeditinglanguages/)(const System::ArrayPtr\<Aspose::Words::Loading::EditingLanguage\>\&) | Добавляет дополнительные языки редактирования. |
| [get_DefaultEditingLanguage](./get_defaulteditinglanguage/)() const | Получает или задает язык редактирования по умолчанию. Значение по умолчанию — [EnglishUS](../editinglanguage/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LanguagePreferences](./languagepreferences/)() |  |
| [set_DefaultEditingLanguage](./set_defaulteditinglanguage/)(Aspose::Words::Loading::EditingLanguage) | Сеттер для [Aspose::Words::Loading::LanguagePreferences::get_DefaultEditingLanguage](./get_defaulteditinglanguage/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как применять предпочтения языка при загрузке документа.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->get_LanguagePreferences()->AddEditingLanguage(Aspose::Words::Loading::EditingLanguage::Japanese);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"No default editing language.docx", loadOptions);

int32_t localeIdFarEast = doc->get_Styles()->get_DefaultFont()->get_LocaleIdFarEast();
std::cout << (localeIdFarEast == (int32_t)Aspose::Words::Loading::EditingLanguage::Japanese ? System::String(u"The document either has no any FarEast language set in defaults or it was set to Japanese originally.") : System::String(u"The document default FarEast language was set to another than Japanese language originally, so it is not overridden.")) << std::endl;
```

## См. также

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
