---
title: LanguagePreferences Class
linktitle: LanguagePreferences
articleTitle: LanguagePreferences
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.LanguagePreferences pour personnaliser et gérer sans effort les paramètres de langue pour un traitement amélioré des documents.
type: docs
weight: 4100
url: /fr/net/aspose.words.loading/languagepreferences/
---
## LanguagePreferences class

Permet de configurer les préférences de langue.

Pour en savoir plus, visitez le[Spécifier les options de chargement](https://docs.aspose.com/words/net/specify-load-options/) article de documentation.

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
| [AddEditingLanguage](../../aspose.words.loading/languagepreferences/addeditinglanguage/)(*[EditingLanguage](../editinglanguage/)*) | Ajoute une langue d'édition supplémentaire. |
| [AddEditingLanguages](../../aspose.words.loading/languagepreferences/addeditinglanguages/)(*EditingLanguage[]*) | Ajoute des langues d'édition supplémentaires. |

## Remarques

Implémente la boîte de dialogue « Définir les préférences linguistiques d'Office » dans Word.

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

* espace de noms [Aspose.Words.Loading](../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../)
