---
title: LanguagePreferences.AddEditingLanguage
linktitle: AddEditingLanguage
articleTitle: AddEditingLanguage
second_title: Aspose.Words pour .NET
description: Améliorez votre expérience d'édition grâce à la méthode AddEditingLanguage de LanguagePreferences. Ajoutez et gérez facilement plusieurs langues d'édition pour un flux de travail fluide.
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

Montre comment appliquer les préférences linguistiques lors du chargement d'un document.

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
