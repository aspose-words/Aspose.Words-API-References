---
title: LoadOptions.LanguagePreferences
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words для .NET
description: Откройте для себя LoadOptions LanguagePreferences, чтобы настроить загрузку документов на предпочитаемых языках, что улучшит пользовательский опыт и доступность.
type: docs
weight: 80
url: /ru/net/aspose.words.loading/loadoptions/languagepreferences/
---
## LoadOptions.LanguagePreferences property

Получает языковые настройки, которые будут использоваться при загрузке документа.

```csharp
public LanguagePreferences LanguagePreferences { get; }
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

* class [LanguagePreferences](../../languagepreferences/)
* class [LoadOptions](../)
* пространство имен [Aspose.Words.Loading](../../../aspose.words.loading/)
* сборка [Aspose.Words](../../../)
