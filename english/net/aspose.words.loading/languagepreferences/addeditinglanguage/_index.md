---
title: AddEditingLanguage
second_title: Aspose.Words for .NET API Reference
description: LanguagePreferences method. Adds additional editing language in C#.
type: docs
weight: 30
url: /net/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences.AddEditingLanguage method

Adds additional editing language.

```csharp
public void AddEditingLanguage(EditingLanguage language)
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

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* namespace [Aspose.Words.Loading](../../languagepreferences/)
* assembly [Aspose.Words](../../../)
