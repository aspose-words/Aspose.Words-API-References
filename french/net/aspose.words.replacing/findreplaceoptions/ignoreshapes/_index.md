---
title: FindReplaceOptions.IgnoreShapes
linktitle: IgnoreShapes
articleTitle: IgnoreShapes
second_title: Aspose.Words pour .NET
description: Découvrez la propriété IgnoreShapes de FindReplaceOptions. Contrôlez l'inclusion des formes dans le traitement de texte grâce à ce paramètre booléen essentiel pour une précision accrue.
type: docs
weight: 110
url: /fr/net/aspose.words.replacing/findreplaceoptions/ignoreshapes/
---
## FindReplaceOptions.IgnoreShapes property

Obtient ou définit une valeur booléenne indiquant d'ignorer les formes dans un texte.

La valeur par défaut est`FAUX`.

```csharp
public bool IgnoreShapes { get; set; }
```

## Exemples

Montre comment ignorer les formes lors du remplacement du texte.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertShape(ShapeType.Balloon, 200, 200);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

FindReplaceOptions findReplaceOptions = new FindReplaceOptions() { IgnoreShapes = true };
builder.Document.Range.Replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
Assert.AreEqual("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.Document.GetText().Trim());
```

### Voir également

* class [FindReplaceOptions](../)
* espace de noms [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* Assemblée [Aspose.Words](../../../)
