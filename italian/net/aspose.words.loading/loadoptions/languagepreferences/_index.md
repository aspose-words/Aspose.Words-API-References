---
title: LoadOptions.LanguagePreferences
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words per .NET
description: Scopri LoadOptions LanguagePreferences per personalizzare il caricamento dei documenti con le lingue preferite, migliorando l'esperienza utente e l'accessibilità.
type: docs
weight: 80
url: /it/net/aspose.words.loading/loadoptions/languagepreferences/
---
## LoadOptions.LanguagePreferences property

Ottiene le preferenze di lingua che verranno utilizzate durante il caricamento del documento.

```csharp
public LanguagePreferences LanguagePreferences { get; }
```

## Esempi

Mostra come applicare le preferenze di lingua durante il caricamento di un documento.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.AddEditingLanguage(EditingLanguage.Japanese);

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeIdFarEast = doc.Styles.DefaultFont.LocaleIdFarEast;
Console.WriteLine(localeIdFarEast == (int)EditingLanguage.Japanese
    ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
    : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
```

### Guarda anche

* class [LanguagePreferences](../../languagepreferences/)
* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
