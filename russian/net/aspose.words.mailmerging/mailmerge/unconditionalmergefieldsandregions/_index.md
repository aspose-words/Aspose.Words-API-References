---
title: MailMerge.UnconditionalMergeFieldsAndRegions
second_title: Справочник по API Aspose.Words для .NET
description: MailMerge свойство. Получает или задает значение указывающее объединяются ли поля слияния и области слияния независимо от условия родительского поля IF.
type: docs
weight: 140
url: /ru/net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

Получает или задает значение, указывающее, объединяются ли поля слияния и области слияния независимо от условия родительского поля IF.

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

### Примечания

Значение по умолчанию: **ЛОЖЬ** .

### Примеры

Показывает, как объединять поля или регионы независимо от условия родительского поля ЕСЛИ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставляем поле MERGEFIELD, вложенное в поле IF.
// Поскольку оператор поля IF неверен, он не будет отображать результат MERGEFIELD.
// MERGEFIELD также не получит никаких данных во время слияния почты.
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// Если мы установим флаг "UnconditionalMergeFieldsAndRegions" в "true",
// наше слияние почты будет вставлять данные в неотображаемые поля, такие как наше MERGEFIELD, а также во все остальные.
// Если мы установим флаг "UnconditionalMergeFieldsAndRegions" в "false",
// наше слияние почты не будет вставлять данные в поля MERGEFIELD, скрытые полями IF с ложными утверждениями.
doc.MailMerge.UnconditionalMergeFieldsAndRegions = countAllMergeFields;

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FullName");
dataTable.Rows.Add("James Bond");

doc.MailMerge.Execute(dataTable);

doc.Save(ArtifactsDir + "MailMerge.UnconditionalMergeFieldsAndRegions.docx");

Assert.AreEqual(
    countAllMergeFields
        ? "\u0013 IF 1 = 2 \"James Bond\"\u0014\u0015"
        : "\u0013 IF 1 = 2 \u0013 MERGEFIELD  FullName \u0014«FullName»\u0015\u0014\u0015",
    doc.GetText().Trim());
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../mailmerge/)
* сборка [Aspose.Words](../../../)


