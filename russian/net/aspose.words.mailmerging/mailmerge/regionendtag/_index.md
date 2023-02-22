---
title: MailMerge.RegionEndTag
second_title: Справочник по API Aspose.Words для .NET
description: MailMerge свойство. Получает или задает конечный тег области слияния.
type: docs
weight: 90
url: /ru/net/aspose.words.mailmerging/mailmerge/regionendtag/
---
## MailMerge.RegionEndTag property

Получает или задает конечный тег области слияния.

```csharp
public string RegionEndTag { get; set; }
```

### Примеры

Показывает, как создавать, перечислять и читать области слияния.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Теги "TableStart" и "TableEnd", которые находятся внутри полей MERGEFIELD,
// обозначают строки, обозначающие начало и конец областей слияния.
Assert.AreEqual("TableStart", doc.MailMerge.RegionStartTag);
Assert.AreEqual("TableEnd", doc.MailMerge.RegionEndTag);

// Используйте эти теги, чтобы начать и закончить область слияния с именем "MailMergeRegion1",
// который будет содержать поля MERGEFIELD для двух столбцов.
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.InsertField(" MERGEFIELD Column1");
builder.Write(", ");
builder.InsertField(" MERGEFIELD Column2");
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Мы можем отслеживать области слияния и их столбцы, просматривая эти коллекции.
IList<MailMergeRegionInfo> regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(1, regions.Count);
Assert.AreEqual("MailMergeRegion1", regions[0].Name);

string[] mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1");

Assert.AreEqual("Column1", mergeFieldNames[0]);
Assert.AreEqual("Column2", mergeFieldNames[1]);

// Вставить регион с таким же именем внутрь существующего региона, что сделает его родительским.
// Теперь поле "Столбец2" будет внутри нового региона.
builder.MoveToField(regions[0].Fields[1], false); 
builder.InsertField(" MERGEFIELD TableStart:MailMergeRegion1");
builder.MoveToField(regions[0].Fields[1], true);
builder.InsertField(" MERGEFIELD TableEnd:MailMergeRegion1");

// Если мы ищем название повторяющихся регионов с помощью метода "GetRegionsByName",
// он вернет все такие регионы в коллекции.
regions = doc.MailMerge.GetRegionsByName("MailMergeRegion1");

Assert.AreEqual(2, regions.Count);
// Проверяем, что второй регион теперь имеет родительский регион.
Assert.AreEqual("MailMergeRegion1", regions[1].ParentRegion.Name);

mergeFieldNames = doc.MailMerge.GetFieldNamesForRegion("MailMergeRegion1", 1);

Assert.AreEqual("Column2", mergeFieldNames[0]);
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge/)
* сборка [Aspose.Words](../../../)


