---
title: CompareOptions.AdvancedOptions
linktitle: AdvancedOptions
articleTitle: AdvancedOptions
second_title: Aspose.Words pour .NET
description: Découvrez les options avancées de CompareOptions pour optimiser vos comparaisons. Obtenez des résultats précis grâce à des paramètres personnalisés pour un résultat optimal.
type: docs
weight: 20
url: /fr/net/aspose.words.comparing/compareoptions/advancedoptions/
---
## CompareOptions.AdvancedOptions property

Spécifie des options de comparaison avancées qui peuvent aider à produire une sortie de comparaison plus précise.

```csharp
public AdvancedCompareOptions AdvancedOptions { get; }
```

## Exemples

Montre comment comparer des documents en ignorant l'ID unique DML.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// Par défaut, Aspose.Words n'ignore pas l'ID unique de DML et le nombre de révisions était de 2.
// Si nous ignorons l'ID unique de DML et que le nombre de révisions était de 0.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### Voir également

* class [AdvancedCompareOptions](../../advancedcompareoptions/)
* class [CompareOptions](../)
* espace de noms [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* Assemblée [Aspose.Words](../../../)
