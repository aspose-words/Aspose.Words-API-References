---
title: Class LanguagePreferences
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Loading.LanguagePreferences klass. Gör det möjligt att ställa in språkinställningar.
type: docs
weight: 3450
url: /sv/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Gör det möjligt att ställa in språkinställningar.

```csharp
public class LanguagePreferences
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [LanguagePreferences](languagepreferences/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DefaultEditingLanguage](../../aspose.words.loading/languagepreferences/defaulteditinglanguage/) { get; set; } | Hämtar eller ställer in standardspråk för redigering. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(EditingLanguage) | Lägger till ytterligare redigeringsspråk. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(EditingLanguage[]) | Lägger till ytterligare redigeringsspråk. |

### Anmärkningar

Implementerar "Ange språkinställningar för Office" i Word.

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

* namnutrymme [Aspose.Words.Loading](../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../)


