---
title: AdvancedCompareOptions Class
linktitle: AdvancedCompareOptions
articleTitle: AdvancedCompareOptions
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.AdvancedCompareOptions pour une comparaison de documents performante. Personnalisez les paramètres pour des résultats précis et une productivité accrue.
type: docs
weight: 460
url: /fr/net/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class

Permet de définir des options de comparaison avancées.

```csharp
public class AdvancedCompareOptions
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [AdvancedCompareOptions](advancedcompareoptions/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/) { get; set; } | Spécifie s'il faut ignorer la différence dans l'identifiant unique de DrawingML. |
| [IgnoreStoreItemId](../../aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/) { get; set; } | Spécifie s'il faut ignorer la différence dans l'ID d'élément de magasin StructuredDocumentTag. |

## Remarques

Ces options n'ont pas d'équivalence dans Microsoft Word et peuvent aider à produire un résultat de comparaison plus précis.

## Exemples

Montre comment comparer SDT avec le même contenu mais un identifiant d'article de magasin différent.

```csharp
Document docA = new Document(MyDir + "Document with SDT 1.docx");
Document docB = new Document(MyDir + "Document with SDT 2.docx");

// Configurez les options pour comparer SDT avec le même contenu mais un identifiant d'élément de magasin différent.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreStoreItemId = false;

docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(8, docA.Revisions.Count);

compareOptions.AdvancedOptions.IgnoreStoreItemId = true;

docA.Revisions.RejectAll();
docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.AreEqual(0, docA.Revisions.Count);
```

### Voir également

* espace de noms [Aspose.Words.Comparing](../../aspose.words.comparing/)
* Assemblée [Aspose.Words](../../)
