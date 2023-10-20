---
title: MailMergeRegionInfo Class
linktitle: MailMergeRegionInfo
articleTitle: MailMergeRegionInfo
second_title: Aspose.Words для .NET
description: Aspose.Words.MailMerging.MailMergeRegionInfo сорт. Содержит информацию о регионе слияния почты на С#.
type: docs
weight: 3860
url: /ru/net/aspose.words.mailmerging/mailmergeregioninfo/
---
## MailMergeRegionInfo class

Содержит информацию о регионе слияния почты.

Чтобы узнать больше, посетите[Слияние почты и отчетность](https://docs.aspose.com/words/net/mail-merge-and-reporting/) статья документации.

```csharp
public class MailMergeRegionInfo
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [EndField](../../aspose.words.mailmerging/mailmergeregioninfo/endfield/) { get; } | Возвращает конечное поле региона. |
| [EndMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/endmustachetag/) { get; } | Возвращает конечный тег «усы» для региона. |
| [Fields](../../aspose.words.mailmerging/mailmergeregioninfo/fields/) { get; } | Возвращает список дочерних полей. |
| [Level](../../aspose.words.mailmerging/mailmergeregioninfo/level/) { get; } | Возвращает уровень вложенности региона. |
| [MustacheTags](../../aspose.words.mailmerging/mailmergeregioninfo/mustachetags/) { get; } | Возвращает список дочерних тегов «усы». |
| [Name](../../aspose.words.mailmerging/mailmergeregioninfo/name/) { get; } | Возвращает название региона. |
| [ParentRegion](../../aspose.words.mailmerging/mailmergeregioninfo/parentregion/) { get; } | Возвращает информацию о родительском регионе (ноль для региона верхнего уровня). |
| [Regions](../../aspose.words.mailmerging/mailmergeregioninfo/regions/) { get; } | Возвращает список дочерних регионов. |
| [StartField](../../aspose.words.mailmerging/mailmergeregioninfo/startfield/) { get; } | Возвращает начальное поле региона. |
| [StartMustacheTag](../../aspose.words.mailmerging/mailmergeregioninfo/startmustachetag/) { get; } | Возвращает начальный тег «усы» для региона. |

## Примеры

Показывает, как проверить регионы слияния почты.

```csharp
Document doc = new Document(MyDir + "Mail merge regions.docx");

// Возвращает полную иерархию областей слияния, содержащих поля MERGEFIELD, доступные в документе.
MailMergeRegionInfo regionInfo = doc.MailMerge.GetRegionsHierarchy();

// Получаем верхние регионы в документе.
IList<MailMergeRegionInfo> topRegions = regionInfo.Regions;

Assert.AreEqual(2, topRegions.Count);
Assert.AreEqual("Region1", topRegions[0].Name);
Assert.AreEqual("Region2", topRegions[1].Name);
Assert.AreEqual(1, topRegions[0].Level);
Assert.AreEqual(1, topRegions[1].Level);

// Получаем вложенный регион в первом верхнем регионе.
IList<MailMergeRegionInfo> nestedRegions = topRegions[0].Regions;

Assert.AreEqual(2, nestedRegions.Count);
Assert.AreEqual("NestedRegion1", nestedRegions[0].Name);
Assert.AreEqual("NestedRegion2", nestedRegions[1].Name);
Assert.AreEqual(2, nestedRegions[0].Level);
Assert.AreEqual(2, nestedRegions[1].Level);

// Получаем список полей внутри первой верхней области.
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
