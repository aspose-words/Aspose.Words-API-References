---
title: AdvancedCompareOptions.IgnoreDmlUniqueId
linktitle: IgnoreDmlUniqueId
articleTitle: IgnoreDmlUniqueId
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IgnoreDmlUniqueId d'AdvancedCompareOptions pour optimiser votre traitement DrawingML en gérant efficacement les identifiants uniques. Optimisez votre flux de travail !
type: docs
weight: 20
url: /fr/net/aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/
---
## AdvancedCompareOptions.IgnoreDmlUniqueId property

Spécifie s'il faut ignorer la différence dans l'identifiant unique de DrawingML.

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

## Remarques

La valeur par défaut est`FAUX` .

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

* class [AdvancedCompareOptions](../)
* espace de noms [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* Assemblée [Aspose.Words](../../../)
