---
title: Class LanguagePreferences
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Loading.LanguagePreferences сорт. Позволяет настроить языковые настройки.
type: docs
weight: 3450
url: /ru/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Позволяет настроить языковые настройки.

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
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(EditingLanguage) | Добавляет дополнительный язык редактирования. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(EditingLanguage[]) | Добавляет дополнительные языки редактирования. |

### Примечания

Реализует диалоговое окно «Установка языковых предпочтений Office» в Word.

### Примеры

Показывает, как применять языковые настройки при загрузке документа.

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


