---
title: LanguagePreferences.AddEditingLanguage
linktitle: AddEditingLanguage
articleTitle: AddEditingLanguage
second_title: Aspose.Words для .NET
description: Улучшите свой опыт редактирования с помощью метода LanguagePreferences AddEditingLanguage. Легко добавляйте и управляйте несколькими языками редактирования для бесперебойного рабочего процесса.
type: docs
weight: 30
url: /ru/net/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences.AddEditingLanguage method

Добавляет дополнительный язык редактирования.

```csharp
public void AddEditingLanguage(EditingLanguage language)
```

## Примеры

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

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
