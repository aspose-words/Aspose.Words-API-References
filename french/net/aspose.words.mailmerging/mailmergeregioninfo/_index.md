---
title: MailMergeRegionInfo Class
linktitle: MailMergeRegionInfo
articleTitle: MailMergeRegionInfo
second_title: Aspose.Words pour .NET
description: Aspose.Words.MailMerging.MailMergeRegionInfo classe. Contient des informations sur une région de publipostage en C#.
type: docs
weight: 3860
url: /fr/net/aspose.words.mailmerging/mailmergeregioninfo/
---
## MailMergeRegionInfo class

Contient des informations sur une région de publipostage.

Pour en savoir plus, visitez le[Fusion et publipostage et création de rapports](https://docs.aspose.com/words/net/mail-merge-and-reporting/) article documentaire.

```csharp
public class MailMergeRegionInfo
```

## Propriétés

| Nom | La description |
| --- | --- |
| [EndField](../../aspose.words.mailmerging/mailmergeregioninfo/endfield/) { get; } | Renvoie un champ de fin pour la région. |
| [EndMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/) { get; } | Renvoie une balise de fin "moustache" pour la région. |
| [Fields](../../aspose.words.mailmerging/mailmergeregioninfo/fields/) { get; } | Renvoie une liste de champs enfants. |
| [Level](../../aspose.words.mailmerging/mailmergeregioninfo/level/) { get; } | Renvoie le niveau d'imbrication pour la région. |
| [MustacheTags](../../aspose.words.mailmerging/mailmergeregioninfo/mustachetags/) { get; } | Renvoie une liste de balises enfants "moustache". |
| [Name](../../aspose.words.mailmerging/mailmergeregioninfo/name/) { get; } | Renvoie le nom de la région. |
| [ParentRegion](../../aspose.words.mailmerging/mailmergeregioninfo/parentregion/) { get; } | Renvoie les informations sur la région parent (null pour la région de niveau supérieur). |
| [Regions](../../aspose.words.mailmerging/mailmergeregioninfo/regions/) { get; } | Renvoie une liste de régions enfants. |
| [StartField](../../aspose.words.mailmerging/mailmergeregioninfo/startfield/) { get; } | Renvoie un champ de début pour la région. |
| [StartMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/) { get; } | Renvoie une balise de début "moustache" pour la région. |

## Exemples

Montre comment vérifier les régions de publipostage.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// Renvoie une hiérarchie complète des régions de fusion contenant les MERGEFIELD disponibles dans le document.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// Récupère les principales régions du document.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// Récupère la région imbriquée dans la première région supérieure.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);

// Récupère la liste des champs à l'intérieur de la première région supérieure.
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### Voir également

* espace de noms [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../)
