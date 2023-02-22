---
title: MailMerge.GetFieldNamesForRegion
second_title: Справочник по API Aspose.Words для .NET
description: MailMerge метод. Возвращает коллекцию имен полей слияния доступных в регионе.
type: docs
weight: 230
url: /ru/net/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## GetFieldNamesForRegion(string) {#getfieldnamesforregion}

Возвращает коллекцию имен полей слияния, доступных в регионе.

```csharp
public string[] GetFieldNamesForRegion(string regionName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| regionName | String | Название региона (без учета регистра). |

### Примечания

Возвращает полные имена полей слияния, включая необязательный префикс. Не устраняет повторяющиеся имена полей.

Если документ содержит несколько регионов с одинаковым названием, обрабатывается самый первый регион.

Новый массив строк создается при каждом вызове.

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

---

## GetFieldNamesForRegion(string, int) {#getfieldnamesforregion_1}

Возвращает коллекцию имен полей слияния, доступных в регионе.

```csharp
public string[] GetFieldNamesForRegion(string regionName, int regionIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| regionName | String | Название региона (без учета регистра). |
| regionIndex | Int32 | Индекс региона (с нуля). |

### Примечания

Возвращает полные имена полей слияния, включая необязательный префикс. Не устраняет повторяющиеся имена полей.

Если документ содержит несколько регионов с одинаковыми именами, обрабатывается N-й регион (начиная с нуля).

Новый массив строк создается при каждом вызове.

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


