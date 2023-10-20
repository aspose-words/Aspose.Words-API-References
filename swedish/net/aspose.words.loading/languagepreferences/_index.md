---
title: LanguagePreferences Class
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words för .NET
description: Aspose.Words.Loading.LanguagePreferences klass. Gör det möjligt att ställa in språkinställningar i C#.
type: docs
weight: 3650
url: /sv/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Gör det möjligt att ställa in språkinställningar.

För att lära dig mer, besök[Ange laddningsalternativ](https://docs.aspose.com/words/net/specify-load-options/) dokumentationsartikel.

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
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(*[EditingLanguage](../editinglanguage/)*) | Lägger till ytterligare redigeringsspråk. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(*EditingLanguage[]*) | Lägger till ytterligare redigeringsspråk. |

## Anmärkningar

Implementerar "Ange språkinställningar för Office" i Word.

## Exempel

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
