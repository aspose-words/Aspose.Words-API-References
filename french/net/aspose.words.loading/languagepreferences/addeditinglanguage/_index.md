---
title: LanguagePreferences.AddEditingLanguage
linktitle: AddEditingLanguage
articleTitle: AddEditingLanguage
second_title: Aspose.Words pour .NET
description: LanguagePreferences AddEditingLanguage méthode. Ajoute une langue dédition supplémentaire en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.loading/languagepreferences/addeditinglanguage/
---
## LanguagePreferences.AddEditingLanguage method

Ajoute une langue d'édition supplémentaire.

```csharp
public void AddEditingLanguage(EditingLanguage language)
```

## Exemples

Montre comment appliquer les préférences de langue lors du chargement d'un document.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.LanguagePreferences.AddEditingLanguage(EditingLanguage.Japanese);

Document doc = new Document(MyDir + "No default editing language.docx", loadOptions);

int localeIdFarEast = doc.Styles.DefaultFont.LocaleIdFarEast;
Console.WriteLine(localeIdFarEast == (int)EditingLanguage.Japanese
    ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
    : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
```

### Voir également

* enum [EditingLanguage](../../editinglanguage/)
* class [LanguagePreferences](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
