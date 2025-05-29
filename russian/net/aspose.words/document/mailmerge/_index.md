---
title: Document.MailMerge
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words для .NET
description: Разблокируйте бесперебойную автоматизацию документооборота с помощью объекта MailMerge, улучшив свой рабочий процесс за счет легкого упрощения задач слияния почты.
type: docs
weight: 270
url: /ru/net/aspose.words/document/mailmerge/
---
## Document.MailMerge property

Возвращает[`MailMerge`](../../../aspose.words.mailmerging/mailmerge/) объект, представляющий функциональность слияния почты для документа.

```csharp
public MailMerge MailMerge { get; }
```

## Примеры

Показывает, как выполнить слияние почты с данными из DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Ниже приведены два способа использования DataTable в качестве источника данных для слияния почты.
    // 1 - Использовать всю таблицу для слияния почты, чтобы создать один выходной документ слияния почты для каждой строки в таблице:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Используйте одну строку таблицы для создания одного выходного документа слияния:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Создает исходный документ для слияния почты.
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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
