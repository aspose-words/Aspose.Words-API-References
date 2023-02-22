---
title: Document.MailMerge
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Возвращает MailMerge объект представляющий функциональность слияния для документа.
type: docs
weight: 240
url: /ru/net/aspose.words/document/mailmerge/
---
## Document.MailMerge property

Возвращает **MailMerge** объект, представляющий функциональность слияния для документа.

```csharp
public MailMerge MailMerge { get; }
```

### Примеры

Показывает, как выполнить слияние почты с данными из DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Ниже приведены два способа использования DataTable в качестве источника данных для слияния.
    // 1 — использовать всю таблицу для слияния, чтобы создать один выходной документ слияния для каждой строки в таблице:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Используйте одну строку таблицы для создания одного выходного документа слияния почты:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Создает исходный документ слияния.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Смотрите также

* class [MailMerge](../../../aspose.words.mailmerging/mailmerge/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


