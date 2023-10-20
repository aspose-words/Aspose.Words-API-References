---
title: LanguagePreferences Class
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words для .NET
description: Aspose.Words.Loading.LanguagePreferences сорт. Позволяет настроить языковые настройки на С#.
type: docs
weight: 3650
url: /ru/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Позволяет настроить языковые настройки.

Чтобы узнать больше, посетите[Укажите параметры загрузки](https://docs.aspose.com/words/net/specify-load-options/) статья документации.

```csharp
public class LanguagePreferences
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [LanguagePreferences](languagepreferences/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DefaultEditingLanguage](../../aspose.words.loading/languagepreferences/defaulteditinglanguage/) { get; set; } | Получает или задает язык редактирования по умолчанию. |

## Методы

| Имя | Описание |
| --- | --- |
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(*[EditingLanguage](../editinglanguage/)*) | Добавляет дополнительный язык редактирования. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(*EditingLanguage[]*) | Добавляет дополнительные языки редактирования. |

## Примечания

Реализует диалоговое окно «Установить языковые настройки Office» в Word.

## Примеры

Показывает, как применить языковые настройки при загрузке документа.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.AddEditingLanguage(EditingLanguage.Japanese);

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeIdFarEast = doc.Styles.DefaultFont.LocaleIdFarEast;
Console.WriteLine(localeIdFarEast == (int)EditingLanguage.Japanese
    ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
    : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
```

### Смотрите также

* пространство имен [Aspose.Words.Loading](../../aspose.words.loading/)
* сборка [Aspose.Words](../../)
