---
title: CompareOptions.Granularity
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words pour .NET
description: Découvrez la propriété de granularité CompareOptions et suivez les modifications par caractère ou par mot pour une édition de texte précise. Améliorez le contrôle de vos documents dès aujourd'hui !
type: docs
weight: 40
url: /fr/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

Spécifie si les modifications sont suivies par caractère ou par mot.

```csharp
public Granularity Granularity { get; set; }
```

## Remarques

La valeur par défaut estWordLevel .

## Exemples

Affiche la spécification d'une granularité lors de la comparaison de documents.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Spécifiez si les modifications sont suivies
// par caractère ('Granularity.CharLevel'), ou par mot ('Granularity.WordLevel').
CompareOptions compareOptions = new CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// La collection de groupes de révision du premier document contient toutes les différences entre les documents.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### Voir également

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* espace de noms [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* Assemblée [Aspose.Words](../../../)
