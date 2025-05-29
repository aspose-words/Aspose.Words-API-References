---
title: LoadOptions.LanguagePreferences
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words för .NET
description: Upptäck LoadOptions LanguagePreferences för att anpassa dokumentinläsning med föredragna språk, vilket förbättrar användarupplevelsen och tillgängligheten.
type: docs
weight: 80
url: /sv/net/aspose.words.loading/loadoptions/languagepreferences/
---
## LoadOptions.LanguagePreferences property

Hämtar språkinställningar som kommer att användas när dokumentet laddas.

```csharp
public LanguagePreferences LanguagePreferences { get; }
```

## Exempel

Visar hur man tillämpar språkinställningar när man laddar ett dokument.

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

* class [LanguagePreferences](../../languagepreferences/)
* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
