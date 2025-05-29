---
title: MailMergeRegionInfo.ParentRegion
linktitle: ParentRegion
articleTitle: ParentRegion
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ParentRegion de MailMergeRegionInfo, qui fournit les informations essentielles sur la région parente et renvoie la valeur null pour les régions de niveau supérieur. Optimisez l'automatisation de vos documents !
type: docs
weight: 70
url: /fr/net/aspose.words.mailmerging/mailmergeregioninfo/parentregion/
---
## MailMergeRegionInfo.ParentRegion property

Renvoie les informations de la région parente (null pour la région de niveau supérieur).

```csharp
public MailMergeRegionInfo ParentRegion { get; }
```

## Exemples

Montre comment créer, répertorier et lire les régions de publipostage.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Les balises « TableStart » et « TableEnd », qui se trouvent à l'intérieur des MERGEFIELD,
// désignent les chaînes qui signifient les débuts et les fins des régions de publipostage.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// Utilisez ces balises pour démarrer et terminer une région de publipostage nommée « MailMergeRegion1 »,
// qui contiendra des MERGEFIELD pour deux colonnes.
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Nous pouvons suivre les régions de fusion et leurs colonnes en consultant ces collections.
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(1, regions.Count);
Assert.AreEqual("MailMergeRegion1", regions[0].Name);

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.AreEqual("Column1", mergeFieldNames[0]);
Assert.AreEqual("Column2", mergeFieldNames[1]);

// Insérez une région avec le même nom à l'intérieur de la région existante, ce qui en fera un parent.
// Désormais, un champ « Colonne 2 » sera à l'intérieur d'une nouvelle région.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Si nous recherchons le nom des régions en double à l'aide de la méthode « GetRegionsByName »,
// il renverra toutes ces régions dans une collection.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// Vérifiez que la deuxième région a désormais une région parent.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### Voir également

* class [MailMergeRegionInfo](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
