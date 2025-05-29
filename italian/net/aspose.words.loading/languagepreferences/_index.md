---
title: LanguagePreferences Class
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.LanguagePreferences per personalizzare e gestire senza sforzo le impostazioni della lingua per un'elaborazione avanzata dei documenti.
type: docs
weight: 4100
url: /it/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Consente di impostare le preferenze della lingua.

Per saperne di più, visita il[Specificare le opzioni di carico](https://docs.aspose.com/words/net/specify-load-options/) articolo di documentazione.

```csharp
public class LanguagePreferences
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [LanguagePreferences](languagepreferences/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DefaultEditingLanguage](../../aspose.words.loading/languagepreferences/defaulteditinglanguage/) { get; set; } | Ottiene o imposta la lingua di modifica predefinita. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(*[EditingLanguage](../editinglanguage/)*) | Aggiunge un linguaggio di modifica aggiuntivo. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(*EditingLanguage[]*) | Aggiunge ulteriori lingue di modifica. |

## Osservazioni

Implementa la finestra di dialogo "Imposta le preferenze di lingua di Office" in Word.

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

* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)
