---
title: MailMergeRegionInfo.MustacheTags
linktitle: MustacheTags
articleTitle: MustacheTags
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MailMergeRegionInfo MustacheTags, которое эффективно возвращает полный список дочерних тегов усов для бесшовной интеграции данных.
type: docs
weight: 50
url: /ru/net/aspose.words.mailmerging/mailmergeregioninfo/mustachetags/
---
## MailMergeRegionInfo.MustacheTags property

Возвращает список дочерних тегов «усы».

```csharp
public IList<MustacheTag> MustacheTags { get; }
```

## Примеры

Показывает, как проверить регионы слияния почты.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// Возвращает полную иерархию областей слияния, содержащих MERGEFIELD, доступные в документе.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// Получить верхние регионы в документе.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// Получить вложенную область в первой верхней области.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);
Assert.AreEqual(0, nestedRegions[1].MustacheTags.Count);

// Получить список полей внутри первой верхней области.
IList<Field> fieldList = topRegions[0].Fields;

Assert.AreEqual(4, fieldList.Count);

FieldMergeField startFieldMergeField = nestedRegions[0].StartField;

Assert.AreEqual("TableStart:NestedRegion1", startFieldMergeField.FieldName);

FieldMergeField endFieldMergeField = nestedRegions[0].EndField;

Assert.AreEqual("TableEnd:NestedRegion1", endFieldMergeField.FieldName);
```

### Смотрите также

* class [MustacheTag](../../mustachetag/)
* class [MailMergeRegionInfo](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
