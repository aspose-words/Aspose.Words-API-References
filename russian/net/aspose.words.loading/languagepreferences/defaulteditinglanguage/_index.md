---
title: LanguagePreferences.DefaultEditingLanguage
linktitle: DefaultEditingLanguage
articleTitle: DefaultEditingLanguage
second_title: Aspose.Words для .NET
description: Управляйте своим опытом редактирования с помощью свойства LanguagePreferences DefaultEditingLanguage. Легко устанавливайте и настраивайте свой язык редактирования по умолчанию.
type: docs
weight: 20
url: /ru/net/aspose.words.loading/languagepreferences/defaulteditinglanguage/
---
## LanguagePreferences.DefaultEditingLanguage property

Получает или задает язык редактирования по умолчанию.

Значение по умолчанию:EnglishUS.

```csharp
public EditingLanguage DefaultEditingLanguage { get; set; }
```

## Примеры

Показывает, как установить язык по умолчанию при загрузке документа.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.DefaultEditingLanguage = EditingLanguage.Russian;

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeId = doc.Styles.DefaultFont.LocaleId;
Console.WriteLine(localeId == (int)EditingLanguage.Russian
    ? "The document either has no any language set in defaults or it was set to Russian originally."
    : "The document default language was set to another than Russian language originally, so it is not overridden.");
```

### Смотрите также

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
