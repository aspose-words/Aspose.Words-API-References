---
title: MailMergeRegionInfo Class
linktitle: MailMergeRegionInfo
articleTitle: MailMergeRegionInfo
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.MailMerging.MailMergeRegionInfo для эффективного управления слиянием почты. Откройте для себя бесперебойную автоматизацию документов сегодня!
type: docs
weight: 4550
url: /ru/net/aspose.words.mailmerging/mailmergeregioninfo/
---
## MailMergeRegionInfo class

Содержит информацию о регионе слияния почты.

Чтобы узнать больше, посетите[Слияние писем и отчетность](https://docs.aspose.com/words/net/mail-merge-and-reporting/) документальная статья.

```csharp
public class MailMergeRegionInfo
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [EndField](../../aspose.words.mailmerging/mailmergeregioninfo/endfield/) { get; } | Возвращает конечное поле для региона. |
| [EndMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/) { get; } | Возвращает конечный тег «усы» для региона. |
| [Fields](../../aspose.words.mailmerging/mailmergeregioninfo/fields/) { get; } | Возвращает список дочерних полей. |
| [Level](../../aspose.words.mailmerging/mailmergeregioninfo/level/) { get; } | Возвращает уровень вложенности для региона. |
| [MustacheTags](../../aspose.words.mailmerging/mailmergeregioninfo/mustachetags/) { get; } | Возвращает список дочерних тегов «усы». |
| [Name](../../aspose.words.mailmerging/mailmergeregioninfo/name/) { get; } | Возвращает название региона. |
| [ParentRegion](../../aspose.words.mailmerging/mailmergeregioninfo/parentregion/) { get; } | Возвращает информацию о родительском регионе (null для региона верхнего уровня). |
| [Regions](../../aspose.words.mailmerging/mailmergeregioninfo/regions/) { get; } | Возвращает список дочерних регионов. |
| [StartField](../../aspose.words.mailmerging/mailmergeregioninfo/startfield/) { get; } | Возвращает начальное поле для региона. |
| [StartMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/) { get; } | Возвращает начальный тег «усы» для региона. |

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

* пространство имен [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../)
