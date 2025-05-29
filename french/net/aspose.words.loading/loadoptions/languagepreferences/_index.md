---
title: LoadOptions.LanguagePreferences
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words pour .NET
description: Découvrez LoadOptions LanguagePreferences pour personnaliser le chargement des documents avec les langues préférées, améliorant ainsi l'expérience utilisateur et l'accessibilité.
type: docs
weight: 80
url: /fr/net/aspose.words.loading/loadoptions/languagepreferences/
---
## LoadOptions.LanguagePreferences property

Obtient les préférences de langue qui seront utilisées lors du chargement du document.

```csharp
public LanguagePreferences LanguagePreferences { get; }
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

* class [LanguagePreferences](../../languagepreferences/)
* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
