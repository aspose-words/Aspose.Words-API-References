---
title: LanguagePreferences.DefaultEditingLanguage
linktitle: DefaultEditingLanguage
articleTitle: DefaultEditingLanguage
second_title: Aspose.Words for .NET
description: Manage your editing experience with the LanguagePreferences DefaultEditingLanguage property. Easily set and customize your default editing language.
type: docs
weight: 20
url: /net/aspose.words.loading/languagepreferences/defaulteditinglanguage/
---
## LanguagePreferences.DefaultEditingLanguage property

Gets or sets default editing language.

The default value is EnglishUS.

```csharp
public EditingLanguage DefaultEditingLanguage { get; set; }
```

## Examples

Shows how set a default language when loading a document.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.DefaultEditingLanguage = EditingLanguage.Russian;

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeId = doc.Styles.DefaultFont.LocaleId;
Console.WriteLine(localeId == (int)EditingLanguage.Russian
    ? "The document either has no any language set in defaults or it was set to Russian originally."
    : "The document default language was set to another than Russian language originally, so it is not overridden.");
```

### See Also

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
