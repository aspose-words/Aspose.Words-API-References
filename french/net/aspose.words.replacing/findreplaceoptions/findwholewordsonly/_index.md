---
title: FindReplaceOptions.FindWholeWordsOnly
linktitle: FindWholeWordsOnly
articleTitle: FindWholeWordsOnly
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété FindWholeWordsOnly améliore votre recherche avec des résultats précis, garantissant que oldValue correspond uniquement en tant que mot autonome.
type: docs
weight: 50
url: /fr/net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

True indique que l'ancienne valeur doit être un mot autonome.

```csharp
public bool FindWholeWordsOnly { get; set; }
```

## Exemples

Montre comment basculer entre les opérations de recherche et de remplacement de mots autonomes uniquement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Nous pouvons utiliser un objet « FindReplaceOptions » pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez l'indicateur « FindWholeWordsOnly » sur « true » pour remplacer le texte trouvé s'il ne fait pas partie d'un autre mot.
// Définissez l'indicateur « FindWholeWordsOnly » sur « false » pour remplacer tout le texte quel que soit son environnement.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)
