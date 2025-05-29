---
title: MailMergeRegionInfo.StartField
linktitle: StartField
articleTitle: StartField
second_title: Aspose.Words pour .NET
description: Découvrez la propriété MailMergeRegionInfo StartField : récupérez efficacement le champ de départ de vos régions de fusion et rationalisez l'automatisation de vos documents.
type: docs
weight: 90
url: /fr/net/aspose.words.mailmerging/mailmergeregioninfo/startfield/
---
## MailMergeRegionInfo.StartField property

Renvoie un champ de départ pour la région.

```csharp
public FieldMergeField StartField { get; }
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

* class [FieldMergeField](../../../aspose.words.fields/fieldmergefield/)
* class [MailMergeRegionInfo](../)
* espace de noms [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Assemblée [Aspose.Words](../../../)
