---
title: MailMerge.UnconditionalMergeFieldsAndRegions
linktitle: UnconditionalMergeFieldsAndRegions
articleTitle: UnconditionalMergeFieldsAndRegions
second_title: Aspose.Words для .NET
description: Узнайте, как свойство UnconditionalMergeFieldsAndRegions в MailMerge улучшает автоматизацию документов за счет объединения полей и областей без условных ограничений.
type: docs
weight: 140
url: /ru/net/aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/
---
## MailMerge.UnconditionalMergeFieldsAndRegions property

Возвращает или задает значение, указывающее, объединяются ли поля слияния и регионы слияния независимо от условия родительского поля IF.

```csharp
public bool UnconditionalMergeFieldsAndRegions { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` .

## Примеры

Показывает, как объединять поля или регионы независимо от условия родительского поля IF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Вставьте MERGEFIELD, вложенный в поле IF.
// Поскольку оператор поля IF является ложным, он не отобразит результат MERGEFIELD.
// MERGEFIELD также не будет получать никаких данных во время слияния почты.
FieldIf fieldIf = (FieldIf)builder.InsertField(" IF 1 = 2 ");
builder.MoveTo(fieldIf.Separator);
builder.InsertField(" MERGEFIELD  FullName ");

// Если мы установим флаг "UnconditionalMergeFieldsAndRegions" в значение "true",
// наше слияние вставит данные в неотображаемые поля, такие как наше MERGEFIELD, а также во все остальные.
// Если мы установим флаг "UnconditionalMergeFieldsAndRegions" на "false",
// наше слияние почты не будет вставлять данные в MERGEFIELD, скрытые полями IF с ложными операторами.
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
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
