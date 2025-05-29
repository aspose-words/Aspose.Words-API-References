---
title: MailMerge.GetFieldNamesForRegion
linktitle: GetFieldNamesForRegion
articleTitle: GetFieldNamesForRegion
second_title: Aspose.Words для .NET
description: Откройте для себя метод MailMerge GetFieldNamesForRegion для легкого доступа к коллекции имен полей слияния в указанном вами регионе. Оптимизируйте свой рабочий процесс!
type: docs
weight: 230
url: /ru/net/aspose.words.mailmerging/mailmerge/getfieldnamesforregion/
---
## GetFieldNamesForRegion(*string*) {#getfieldnamesforregion}

Возвращает коллекцию имен полей слияния, доступных в регионе.

```csharp
public string[] GetFieldNamesForRegion(string regionName)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| regionName | String | Название региона (без учета регистра). |

## Примечания

Возвращает полные имена полей слияния, включая необязательный префикс. Не устраняет дублирующиеся имена полей.

Если документ содержит несколько регионов с одинаковым именем, обрабатывается самый первый регион.

При каждом вызове создается новый массив строк.

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

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)

---

## GetFieldNamesForRegion(*string, int*) {#getfieldnamesforregion_1}

Возвращает коллекцию имен полей слияния, доступных в регионе.

```csharp
public string[] GetFieldNamesForRegion(string regionName, int regionIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| regionName | String | Название региона (без учета регистра). |
| regionIndex | Int32 | Индекс региона (отсчет начинается с нуля). |

## Примечания

Возвращает полные имена полей слияния, включая необязательный префикс. Не устраняет дублирующиеся имена полей.

Если документ содержит несколько регионов с одинаковым именем, обрабатывается N-й регион (начиная с нуля).

При каждом вызове создается новый массив строк.

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

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
