---
title: LanguagePreferences
second_title: Aspose.Words per .NET API Reference
description: Consente di impostare le preferenze della lingua.
type: docs
weight: 3450
url: /it/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Consente di impostare le preferenze della lingua.

```csharp
public class LanguagePreferences
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [LanguagePreferences](languagepreferences)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DefaultEditingLanguage](../../aspose.words.loading/languagepreferences/defaulteditinglanguage) { get; set; } | Ottiene o imposta la lingua di modifica predefinita. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage)(EditingLanguage) | Aggiunge un linguaggio di modifica aggiuntivo. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages)(EditingLanguage[]) | Aggiunge lingue di modifica aggiuntive. |

### Osservazioni

Implementa la finestra di dialogo "Imposta le preferenze della lingua di Office" in Word.

### Esempi

Mostra come applicare le preferenze della lingua durante il caricamento di un documento.

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

* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
