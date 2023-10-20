---
title: MailMerge.UseWholeParagraphAsRegion
linktitle: UseWholeParagraphAsRegion
articleTitle: UseWholeParagraphAsRegion
second_title: Aspose.Words для .NET
description: MailMerge UseWholeParagraphAsRegion свойство. Получает или задает значение указывающее содержит ли весь абзацТаблеСтарт илиКонец таблицы field или определенный диапазон междуТаблеСтарт иКонец таблицы поля должны быть включены в регион слияния почты на С#.
type: docs
weight: 160
url: /ru/net/aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/
---
## MailMerge.UseWholeParagraphAsRegion property

Получает или задает значение, указывающее, содержит ли весь абзац**ТаблеСтарт** или**Конец таблицы** field или определенный диапазон между**ТаблеСтарт** и**Конец таблицы** поля должны быть включены в регион слияния почты.

```csharp
public bool UseWholeParagraphAsRegion { get; set; }
```

## Примечания

Значение по умолчанию:`истинный` .

## Примеры

Показывает связь между областями слияния почты и абзацами.

```csharp
public void UseWholeParagraphAsRegion(bool useWholeParagraphAsRegion)
{
    Document doc = CreateSourceDocWithNestedMergeRegions();
    DataTable dataTable = CreateSourceTableDataTableForOneRegion();

    // По умолчанию абзац может принадлежать не более чем к одному региону слияния почты.
    // Содержимое нашего документа не соответствует этим критериям.
    // Если мы установим флаг «UseWholeParagraphAsRegion» в значение «true»,
    // запуск слияния почты для этого документа вызовет исключение.
    // Если мы установим флаг «UseWholeParagraphAsRegion» в значение «false»,
    // мы сможем выполнить слияние почты для этого документа.
    doc.MailMerge.UseWholeParagraphAsRegion = useWholeParagraphAsRegion;

    if (useWholeParagraphAsRegion)
        Assert.Throws<InvalidOperationException>(() => doc.MailMerge.ExecuteWithRegions(dataTable));
    else
        doc.MailMerge.ExecuteWithRegions(dataTable);

    // Слияние почты заполняет наш первый регион, оставляя второй регион неиспользованным
    // так как именно этот регион нарушает правило.
    doc.Save(ArtifactsDir + "MailMerge.UseWholeParagraphAsRegion.docx");
}

/// <summary>
/// Создайте документ с двумя областями слияния почты, разделяющими один абзац.
/// </summary>
private static Document CreateSourceDocWithNestedMergeRegions()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Write("Region 1: ");
    builder.InsertField(" MERGEFIELD TableStart:MyTable");
    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column2");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    builder.Write(", Region 2: ");
    builder.InsertField(" MERGEFIELD TableStart:MyOtherTable");
    builder.InsertField(" MERGEFIELD TableEnd:MyOtherTable");

    return doc;
}

/// <summary>
/// Создайте таблицу данных, которая может заполнить один регион во время слияния почты.
/// </summary>
private static DataTable CreateSourceTableDataTableForOneRegion()
{
    DataTable dataTable = new DataTable("MyTable");
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
