---
title: MailMerge.MergeDuplicateRegions
linktitle: MergeDuplicateRegions
articleTitle: MergeDuplicateRegions
second_title: Aspose.Words для .NET
description: Оптимизируйте процесс слияния почты с помощью свойства MergeDuplicateRegions. Контролируйте, как объединяются области источника данных для эффективного управления документами.
type: docs
weight: 60
url: /ru/net/aspose.words.mailmerging/mailmerge/mergeduplicateregions/
---
## MailMerge.MergeDuplicateRegions property

Возвращает или задает значение, указывающее, следует ли объединять все регионы слияния почты документа с именем источника данных при выполнении слияния почты с регионами по отношению к источнику данных или только первый из них.

```csharp
public bool MergeDuplicateRegions { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` .

## Примеры

Показывает, как работать с дублирующимися областями слияния почты.

```csharp
public void MergeDuplicateRegions(bool mergeDuplicateRegions)
{
    Document doc = CreateSourceDocMergeDuplicateRegions();
    DataTable dataTable = CreateSourceTableMergeDuplicateRegions();

    // Если мы установим свойство "MergeDuplicateRegions" в значение "false", слияние повлияет на первый регион,
    // в то время как MERGEFIELD второго останутся в состоянии до слияния.
    // Чтобы объединить оба региона таким образом,
    // нам пришлось бы выполнить слияние дважды для таблицы с одним и тем же именем.
    // Если мы установим свойство «MergeDuplicateRegions» в значение «true», слияние почты затронет оба региона.
    doc.MailMerge.MergeDuplicateRegions = mergeDuplicateRegions;

    doc.MailMerge.ExecuteWithRegions(dataTable);
    doc.Save(ArtifactsDir + "MailMerge.MergeDuplicateRegions.docx");
}

/// <summary>
/// Возвращает документ, содержащий две дублирующиеся области слияния почты (имеющие одинаковое имя в тегах «TableStart/End»).
/// </summary>
private static Document CreateSourceDocMergeDuplicateRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column1");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD TableStart:MergeRegion");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MergeRegion");

    return doc;
}

/// <summary>
/// Создает таблицу данных с одной строкой и двумя столбцами.
/// </summary>
private static DataTable CreateSourceTableMergeDuplicateRegions()
{
    DataTable dataTable = new DataTable("MergeRegion");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value 1", "Value 2" });

    return dataTable;
}
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
