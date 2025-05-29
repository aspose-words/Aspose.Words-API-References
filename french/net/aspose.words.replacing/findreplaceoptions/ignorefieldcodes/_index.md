---
title: FindReplaceOptions.IgnoreFieldCodes
linktitle: IgnoreFieldCodes
articleTitle: IgnoreFieldCodes
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IgnoreFieldCodes de FindReplaceOptions pour gérer facilement le texte des codes de champ. Contrôlez la visibilité avec un simple paramètre booléen !
type: docs
weight: 70
url: /fr/net/aspose.words.replacing/findreplaceoptions/ignorefieldcodes/
---
## FindReplaceOptions.IgnoreFieldCodes property

Obtient ou définit une valeur booléenne indiquant d'ignorer le texte à l'intérieur des codes de champ. La valeur par défaut est`FAUX` .

```csharp
public bool IgnoreFieldCodes { get; set; }
```

## Remarques

Cette option affecte uniquement les codes de champ (elle n'ignore pas les nœuds entre FieldSeparator etFieldEnd).

Pour ignorer l'ensemble du champ, veuillez utiliser l'option correspondante[`IgnoreFields`](../ignorefields/).

## Exemples

Montre comment ignorer le texte à l'intérieur des codes de champ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("INCLUDETEXT", "Test IT!");

FindReplaceOptions options = new FindReplaceOptions {IgnoreFieldCodes = ignoreFieldCodes};

// Remplacez « T » dans le document en ignorant le texte à l'intérieur du code de champ ou non.
doc.Range.Replace(new Regex("T"), "*", options);
Console.WriteLine(doc.GetText());

Assert.AreEqual(
    ignoreFieldCodes
        ? "\u0013INCLUDETEXT\u0014*est I*!\u0015"
        : "\u0013INCLUDE*EX*\u0014*est I*!\u0015", doc.GetText().Trim());
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)
