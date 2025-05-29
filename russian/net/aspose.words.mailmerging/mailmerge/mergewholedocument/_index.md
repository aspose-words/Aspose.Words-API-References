---
title: MailMerge.MergeWholeDocument
linktitle: MergeWholeDocument
articleTitle: MergeWholeDocument
second_title: Aspose.Words для .NET
description: Узнайте, как свойство MailMerge MergeWholeDocument обновляет все поля во время регионального слияния почты, повышая эффективность и точность ваших документов.
type: docs
weight: 70
url: /ru/net/aspose.words.mailmerging/mailmerge/mergewholedocument/
---
## MailMerge.MergeWholeDocument property

Возвращает или задает значение, указывающее, обновляются ли поля во всем документе при выполнении слияния почты с регионами.

```csharp
public bool MergeWholeDocument { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ` .

## Примеры

Показывает связь между слияниями почты с регионами и обновлением полей.

```csharp
public void MergeWholeDocument(bool mergeWholeDocument)
{
    Document doc = CreateSourceDocMergeWholeDocument();
    DataTable dataTable = CreateSourceTableMergeWholeDocument();

    // Если мы установим флаг "MergeWholeDocument" на "true",
    // слияние почты с регионами обновит каждое поле в документе.
    // Если мы установим флаг «MergeWholeDocument» на «false», слияние почты обновит только поля
    // в области слияния почты, имя которой совпадает с именем таблицы источника данных.
    doc.MailMerge.MergeWholeDocument = mergeWholeDocument;
    doc.MailMerge.ExecuteWithRegions(dataTable);

    // Слияние почты обновит только поле ЦИТАТА за пределами области слияния почты
    // если мы установим флаг "MergeWholeDocument" в значение "true".
    doc.Save(ArtifactsDir + "MailMerge.MergeWholeDocument.docx");

    Assert.True(doc.GetText().Contains("This QUOTE field is inside the \"MyTable\" merge region."));
    Assert.AreEqual(mergeWholeDocument, 
        doc.GetText().Contains("This QUOTE field is outside of the \"MyTable\" merge region."));
}

/// <summary>
/// Создайте документ с областью слияния почты, принадлежащей источнику данных с именем «MyTable».
/// Вставьте одно поле QUOTE внутри этой области и еще одно снаружи.
/// </summary>
private static Document CreateSourceDocMergeWholeDocument()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    FieldQuote field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is outside of the \"MyTable\" merge region.";

    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD TableStart:MyTable");

    field = (FieldQuote)builder.InsertField(FieldType.FieldQuote, true);
    field.Text = "This QUOTE field is inside the \"MyTable\" merge region.";
    builder.InsertParagraph();

    builder.InsertField(" MERGEFIELD MyColumn");
    builder.InsertField(" MERGEFIELD TableEnd:MyTable");

    return doc;
}

/// <summary>
/// Создайте таблицу данных, которая будет использоваться при слиянии писем.
/// </summary>
private static DataTable CreateSourceTableMergeWholeDocument()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("MyColumn");
    dataTable.Rows.Add(new object[] { "MyValue" });

    return dataTable;
}
```

### Смотрите также

* class [MailMerge](../)
* пространство имен [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* сборка [Aspose.Words](../../../)
