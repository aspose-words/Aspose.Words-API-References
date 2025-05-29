---
title: LanguagePreferences Class
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.LanguagePreferences, um Spracheinstellungen für eine verbesserte Dokumentverarbeitung mühelos anzupassen und zu verwalten.
type: docs
weight: 4100
url: /de/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Ermöglicht das Einrichten von Spracheinstellungen.

Um mehr zu erfahren, besuchen Sie die[Ladeoptionen festlegen](https://docs.aspose.com/words/net/specify-load-options/) Dokumentationsartikel.

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
| [DefaultEditingLanguage](../../aspose.words.loading/languagepreferences/defaulteditinglanguage/) { get; set; } | Ruft die Standardbearbeitungssprache ab oder legt sie fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(*[EditingLanguage](../editinglanguage/)*) | Fügt zusätzliche Bearbeitungssprache hinzu. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(*EditingLanguage[]*) | Fügt zusätzliche Bearbeitungssprachen hinzu. |

## Bemerkungen

Implementiert das Dialogfeld „Office-Spracheinstellungen festlegen“ in Word.

## Beispiele

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
