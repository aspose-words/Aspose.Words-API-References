---
title: LanguagePreferences.DefaultEditingLanguage
linktitle: DefaultEditingLanguage
articleTitle: DefaultEditingLanguage
second_title: Aspose.Words för .NET
description: Hantera din redigeringsupplevelse med egenskapen LanguagePreferences DefaultEditingLanguage. Ställ enkelt in och anpassa ditt standardredigeringsspråk.
type: docs
weight: 20
url: /sv/net/aspose.words.loading/languagepreferences/defaulteditinglanguage/
---
## LanguagePreferences.DefaultEditingLanguage property

Hämtar eller ställer in standardredigeringsspråk.

Standardvärdet ärEnglishUS.

```csharp
public EditingLanguage DefaultEditingLanguage { get; set; }
```

## Exempel

Visar hur man ställer in ett standardspråk när man laddar ett dokument.

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
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
