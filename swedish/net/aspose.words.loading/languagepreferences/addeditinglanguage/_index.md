---
title: LanguagePreferences.AddEditingLanguage
second_title: Aspose.Words för .NET API Referens
description: LanguagePreferences metod. Lägger till ytterligare redigeringsspråk.
type: docs
weight: 30
url: /sv/net/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences.AddEditingLanguage method

Lägger till ytterligare redigeringsspråk.

```csharp
public void AddEditingLanguage(EditingLanguage language)
```

### Exempel

Visar hur du använder språkinställningar när du laddar ett dokument.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.AddEditingLanguage(EditingLanguage.Japanese);

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeIdFarEast = doc.Styles.DefaultFont.LocaleIdFarEast;
Console.WriteLine(localeIdFarEast == (int)EditingLanguage.Japanese
    ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
    : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
```

### Se även

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* namnutrymme [Aspose.Words.Loading](../../languagepreferences/)
* hopsättning [Aspose.Words](../../../)


