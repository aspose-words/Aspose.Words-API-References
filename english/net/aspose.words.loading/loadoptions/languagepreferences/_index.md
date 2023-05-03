---
title: LoadOptions.LanguagePreferences
linktitle: LanguagePreferences
second_title: Aspose.Words for .NET API Reference
description: LoadOptions LanguagePreferences property. Gets language preferences that will be used when document is loading in C#.
type: docs
weight: 80
url: /net/aspose.words.loading/loadoptions/languagepreferences/
---
## LanguagePreferences property

Gets language preferences that will be used when document is loading.

```csharp
public LanguagePreferences LanguagePreferences { get; }
```

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

* class [LanguagePreferences](../../languagepreferences/)
* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../loadoptions/)
* assembly [Aspose.Words](../../../)
