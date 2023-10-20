---
title: LanguagePreferences.DefaultEditingLanguage
linktitle: DefaultEditingLanguage
articleTitle: DefaultEditingLanguage
second_title: Aspose.Words per .NET
description: LanguagePreferences DefaultEditingLanguage proprietà. Ottiene o imposta la lingua di modifica predefinita in C#.
type: docs
weight: 20
url: /it/net/aspose.words.loading/languagepreferences/defaulteditinglanguage/
---
## LanguagePreferences.DefaultEditingLanguage property

Ottiene o imposta la lingua di modifica predefinita.

Il valore predefinito èEnglishUS.

```csharp
public EditingLanguage DefaultEditingLanguage { get; set; }
```

## Esempi

Mostra come impostare una lingua predefinita durante il caricamento di un documento.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.DefaultEditingLanguage = EditingLanguage.Russian;

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeId = doc.Styles.DefaultFont.LocaleId;
Console.WriteLine(localeId == (int)EditingLanguage.Russian
    ? "The document either has no any language set in defaults or it was set to Russian originally."
    : "The document default language was set to another than Russian language originally, so it is not overridden.");
```

### Guarda anche

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
