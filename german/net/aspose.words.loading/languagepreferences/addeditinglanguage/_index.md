---
title: LanguagePreferences.AddEditingLanguage
linktitle: AddEditingLanguage
articleTitle: AddEditingLanguage
second_title: Aspose.Words für .NET
description: Verbessern Sie Ihr Bearbeitungserlebnis mit der AddEditingLanguage-Methode von LanguagePreferences. Fügen Sie einfach mehrere Bearbeitungssprachen hinzu und verwalten Sie sie für einen reibungslosen Arbeitsablauf.
type: docs
weight: 30
url: /de/net/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences.AddEditingLanguage method

Fügt zusätzliche Bearbeitungssprache hinzu.

```csharp
public void AddEditingLanguage(EditingLanguage language)
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

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
