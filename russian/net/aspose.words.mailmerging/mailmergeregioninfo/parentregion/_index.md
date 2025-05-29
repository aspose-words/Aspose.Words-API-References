---
title: MailMergeRegionInfo.ParentRegion
linktitle: ParentRegion
articleTitle: ParentRegion
second_title: Aspose.Words для .NET
description: Откройте для себя свойство MailMergeRegionInfo ParentRegion, которое предоставляет основные сведения о родительском регионе, возвращая null для регионов верхнего уровня. Улучшите автоматизацию документов!
type: docs
weight: 70
url: /ru/net/aspose.words.mailmerging/mailmergeregioninfo/parentregion/
---
## MailMergeRegionInfo.ParentRegion property

Возвращает информацию о родительском регионе (null для региона верхнего уровня).

```csharp
public MailMergeRegionInfo ParentRegion { get; }
```

## Примеры

Показывает, как создавать, перечислять и читать регионы слияния почты.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Теги "TableStart" и "TableEnd", которые находятся внутри MERGEFIELD,
// обозначают строки, которые обозначают начало и конец областей слияния почты.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// Используйте эти теги для начала и завершения региона слияния почты с именем «MailMergeRegion1»,
// который будет содержать MERGEFIELD для двух столбцов.
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Мы можем отслеживать регионы слияния и их столбцы, просматривая эти коллекции.
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(1, regions.Count);
Assert.AreEqual("MailMergeRegion1", regions[0].Name);

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.AreEqual("Column1", mergeFieldNames[0]);
Assert.AreEqual("Column2", mergeFieldNames[1]);

// Вставляем регион с тем же именем внутрь существующего региона, что делает его родительским.
// Теперь поле «Столбец2» будет находиться внутри новой области.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Если мы ищем имя дублирующихся регионов с помощью метода "GetRegionsByName",
// он вернет все такие регионы в коллекции.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// Проверяем, что у второго региона теперь есть родительский регион.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### Смотрите также

* class [MailMergeRegionInfo](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
