---
title: LoadOptions.LanguagePreferences
second_title: Aspose.Words für .NET-API-Referenz
description: LoadOptions eigendom. Ruft Spracheinstellungen ab die beim Laden des Dokuments verwendet werden.
type: docs
weight: 80
url: /de/net/aspose.words.loading/loadoptions/languagepreferences/
---
## LoadOptions.LanguagePreferences property

Ruft Spracheinstellungen ab, die beim Laden des Dokuments verwendet werden.

```csharp
public LanguagePreferences LanguagePreferences { get; }
```

### Beispiele

Zeigt, wie Spracheinstellungen beim Laden eines Dokuments angewendet werden.

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
* namensraum [Aspose.Words.Loading](../../loadoptions/)
* Montage [Aspose.Words](../../../)


