---
title: FindReplaceOptions.FindWholeWordsOnly
second_title: Référence de l'API Aspose.Words pour .NET
description: FindReplaceOptions propriété. True indique que lancienne valeur doit être un mot autonome.
type: docs
weight: 50
url: /fr/net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

True indique que l'ancienne valeur doit être un mot autonome.

```csharp
public bool FindWholeWordsOnly { get; set; }
```

### Exemples

Montre comment basculer les opérations autonomes de recherche et de remplacement de mots uniquement.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Nous pouvons utiliser un objet "FindReplaceOptions" pour modifier le processus de recherche et de remplacement.
FindReplaceOptions options = new FindReplaceOptions();

// Définissez le drapeau "FindWholeWordsOnly" sur "true" pour remplacer le texte trouvé s'il ne fait pas partie d'un autre mot.
// Définissez le drapeau "FindWholeWordsOnly" sur "false" pour remplacer tout le texte quel que soit son environnement.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../findreplaceoptions/)
* Assemblée [Aspose.Words](../../../)


