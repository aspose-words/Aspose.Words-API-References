---
title: MailMergeRegionInfo.MustacheTags
linktitle: MustacheTags
articleTitle: MustacheTags
second_title: Aspose.Words pour .NET
description: Découvrez la propriété MailMergeRegionInfo MustacheTags, qui renvoie efficacement une liste complète de balises moustache enfants pour une intégration transparente des données.
type: docs
weight: 50
url: /fr/net/aspose.words.mailmerging/mailmergeregioninfo/mustachetags/
---
## MailMergeRegionInfo.MustacheTags property

Renvoie une liste de balises « moustache » enfants.

```csharp
public IList<MustacheTag> MustacheTags { get; }
```

## Exemples

Montre comment vérifier les régions de publipostage.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// Renvoie une hiérarchie complète des régions de fusion qui contiennent les MERGEFIELD disponibles dans le document.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// Obtenir les principales régions du document.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// Obtenir la région imbriquée dans la première région supérieure.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);
Assert.AreEqual(0, nestedRegions[1].MustacheTags.Count);

// Obtenir la liste des champs à l'intérieur de la première région supérieure.
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### Voir également

* class [MustacheTag](../../mustachetag/)
* class [MailMergeRegionInfo](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
