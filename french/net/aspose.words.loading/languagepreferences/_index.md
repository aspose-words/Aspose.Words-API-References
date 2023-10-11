---
title: Class LanguagePreferences
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Loading.LanguagePreferences classe. Permet de configurer les préférences de langue.
type: docs
weight: 3650
url: /fr/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Permet de configurer les préférences de langue.

Pour en savoir plus, visitez le[Spécifier les options de chargement](https://docs.aspose.com/words/net/specify-load-options/) article documentaire.

```csharp
public class LanguagePreferences
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [LanguagePreferences](languagepreferences/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [DefaultEditingLanguage](../../aspose.words.loading/languagepreferences/defaulteditinglanguage/) { get; set; } | Obtient ou définit la langue d'édition par défaut. |

## Méthodes

| Nom | La description |
| --- | --- |
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(EditingLanguage) | Ajoute une langue d'édition supplémentaire. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(EditingLanguage[]) | Ajoute des langues d'édition supplémentaires. |

### Remarques

Implémente la boîte de dialogue « Définir les préférences linguistiques d'Office » dans Word.

### Exemples

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

* espace de noms [Aspose.Words.Loading](../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../)


