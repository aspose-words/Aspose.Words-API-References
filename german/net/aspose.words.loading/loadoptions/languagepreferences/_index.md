---
title: LoadOptions.LanguagePreferences
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words für .NET
description: Entdecken Sie LoadOptions LanguagePreferences, um das Laden von Dokumenten mit bevorzugten Sprachen anzupassen und so Benutzerfreundlichkeit und Zugänglichkeit zu verbessern.
type: docs
weight: 80
url: /de/net/aspose.words.loading/loadoptions/languagepreferences/
---
## LoadOptions.LanguagePreferences property

Ruft die Spracheinstellungen ab, die beim Laden des Dokuments verwendet werden.

```csharp
public LanguagePreferences LanguagePreferences { get; }
```

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

* class [LanguagePreferences](../../languagepreferences/)
* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
