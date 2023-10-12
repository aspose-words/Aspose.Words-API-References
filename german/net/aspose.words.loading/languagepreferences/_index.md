---
title: Class LanguagePreferences
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Loading.LanguagePreferences klas. Ermöglicht das Einrichten von Spracheinstellungen.
type: docs
weight: 3650
url: /de/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Ermöglicht das Einrichten von Spracheinstellungen.

Um mehr zu erfahren, besuchen Sie die[Geben Sie Ladeoptionen an](https://docs.aspose.com/words/net/specify-load-options/) Dokumentationsartikel.

```csharp
public class LanguagePreferences
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [LanguagePreferences](languagepreferences/)() | Default_Constructor |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [DefaultEditingLanguage](../../aspose.words.loading/languagepreferences/defaulteditinglanguage/) { get; set; } | Ruft die Standardbearbeitungssprache ab oder legt diese fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(EditingLanguage) | Fügt zusätzliche Bearbeitungssprache hinzu. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(EditingLanguage[]) | Fügt zusätzliche Bearbeitungssprachen hinzu. |

### Bemerkungen

Implementiert das Dialogfeld „Office-Spracheinstellungen festlegen“ in Word.

### Beispiele

Zeigt, wie beim Laden eines Dokuments Spracheinstellungen angewendet werden.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.AddEditingLanguage(EditingLanguage.Japanese);

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeIdFarEast = doc.Styles.DefaultFont.LocaleIdFarEast;
Console.WriteLine(localeIdFarEast == (int)EditingLanguage.Japanese
    ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
    : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
```

### Siehe auch

* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)


