---
title: LanguagePreferences.DefaultEditingLanguage
second_title: Aspose.Words för .NET API Referens
description: LanguagePreferences fast egendom. Hämtar eller ställer in standardspråk för redigering.
type: docs
weight: 20
url: /sv/net/aspose.words.loading/languagepreferences/defaulteditinglanguage/
---
## LanguagePreferences.DefaultEditingLanguage property

Hämtar eller ställer in standardspråk för redigering.

Standardvärdet ärEnglishUS.

```csharp
public EditingLanguage DefaultEditingLanguage { get; set; }
```

### Exempel

Visar hur man ställer in ett standardspråk när ett dokument laddas.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.DefaultEditingLanguage = EditingLanguage.Russian;

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeId = doc.Styles.DefaultFont.LocaleId;
Console.WriteLine(localeId == (int)EditingLanguage.Russian
    ? "The document either has no any language set in defaults or it was set to Russian originally."
    : "The document default language was set to another than Russian language originally, so it is not overridden.");
```

### Se även

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* namnutrymme [Aspose.Words.Loading](../../languagepreferences/)
* hopsättning [Aspose.Words](../../../)


