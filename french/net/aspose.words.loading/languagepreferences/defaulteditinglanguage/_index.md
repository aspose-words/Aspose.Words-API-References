---
title: LanguagePreferences.DefaultEditingLanguage
linktitle: DefaultEditingLanguage
articleTitle: DefaultEditingLanguage
second_title: Aspose.Words pour .NET
description: Gérez votre expérience d'édition grâce à la propriété « DefaultEditingLanguage » de LanguagePreferences. Définissez et personnalisez facilement votre langue d'édition par défaut.
type: docs
weight: 20
url: /fr/net/aspose.words.loading/languagepreferences/defaulteditinglanguage/
---
## LanguagePreferences.DefaultEditingLanguage property

Obtient ou définit la langue d'édition par défaut.

La valeur par défaut estEnglishUS.

```csharp
public EditingLanguage DefaultEditingLanguage { get; set; }
```

## Exemples

Montre comment définir une langue par défaut lors du chargement d'un document.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.DefaultEditingLanguage = EditingLanguage.Russian;

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeId = doc.Styles.DefaultFont.LocaleId;
Console.WriteLine(localeId == (int)EditingLanguage.Russian
    ? "The document either has no any language set in defaults or it was set to Russian originally."
    : "The document default language was set to another than Russian language originally, so it is not overridden.");
```

### Voir également

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
