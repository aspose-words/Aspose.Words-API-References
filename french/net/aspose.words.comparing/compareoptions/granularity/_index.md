---
title: CompareOptions.Granularity
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words pour .NET
description: CompareOptions Granularity propriété. Spécifie si les modifications sont suivies par caractère ou par mot. La valeur par défaut estWordLevel  en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

Spécifie si les modifications sont suivies par caractère ou par mot. La valeur par défaut estWordLevel .

```csharp
public Granularity Granularity { get; set; }
```

## Exemples

Montre pour spécifier une granularité lors de la comparaison de documents.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// Spécifie si les modifications sont suivies
// par caractère ('Granularity.CharLevel'), ou par mot ('Granularity.WordLevel').
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
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
