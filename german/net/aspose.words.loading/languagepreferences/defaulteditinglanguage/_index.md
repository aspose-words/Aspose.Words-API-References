---
title: LanguagePreferences.DefaultEditingLanguage
linktitle: DefaultEditingLanguage
articleTitle: DefaultEditingLanguage
second_title: Aspose.Words für .NET
description: LanguagePreferences DefaultEditingLanguage eigendom. Ruft die Standardbearbeitungssprache ab oder legt diese fest in C#.
type: docs
weight: 20
url: /de/net/aspose.words.loading/languagepreferences/defaulteditinglanguage/
---
## LanguagePreferences.DefaultEditingLanguage property

Ruft die Standardbearbeitungssprache ab oder legt diese fest.

Der Standardwert istEnglishUS.

```csharp
public EditingLanguage DefaultEditingLanguage { get; set; }
```

## Beispiele

Zeigt, wie beim Laden eines Dokuments eine Standardsprache festgelegt wird.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.DefaultEditingLanguage = EditingLanguage.Russian;

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeId = doc.Styles.DefaultFont.LocaleId;
Console.WriteLine(localeId == (int)EditingLanguage.Russian
    ? "The document either has no any language set in defaults or it was set to Russian originally."
    : "The document default language was set to another than Russian language originally, so it is not overridden.");
```

### Siehe auch

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
