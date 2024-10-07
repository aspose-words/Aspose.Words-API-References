---
title: LanguagePreferences Class
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words for .NET
description: Aspose.Words.Loading.LanguagePreferences class. Allows to set up language preferences in C#.
type: docs
weight: 3950
url: /net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Allows to set up language preferences.

To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/net/specify-load-options/) documentation article.

```csharp
public class LanguagePreferences
```

## Constructors

| Name | Description |
| --- | --- |
| [LanguagePreferences](languagepreferences/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [DefaultEditingLanguage](../../aspose.words.loading/languagepreferences/defaulteditinglanguage/) { get; set; } | Gets or sets default editing language. |

## Methods

| Name | Description |
| --- | --- |
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(*[EditingLanguage](../editinglanguage/)*) | Adds additional editing language. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(*EditingLanguage[]*) | Adds additional editing languages. |

## Remarks

Implements 'Set the Office Language Preferences' dialog in Word.

## Examples

Shows how to apply language preferences when loading a document.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.AddEditingLanguage(EditingLanguage.Japanese);

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeIdFarEast = doc.Styles.DefaultFont.LocaleIdFarEast;
Console.WriteLine(localeIdFarEast == (int)EditingLanguage.Japanese
    ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
    : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
```

### See Also

* namespace [Aspose.Words.Loading](../../aspose.words.loading/)
* assembly [Aspose.Words](../../)
