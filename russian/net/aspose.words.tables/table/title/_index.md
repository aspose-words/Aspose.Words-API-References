---
title: Table.Title
second_title: Справочник по API Aspose.Words для .NET
description: Table свойство. Получает или задает заголовок этой таблицы. Предоставляет альтернативное текстовое представление информации содержащейся в таблице.
type: docs
weight: 320
url: /ru/net/aspose.words.tables/table/title/
---
## Table.Title property

Получает или задает заголовок этой таблицы. Предоставляет альтернативное текстовое представление информации, содержащейся в таблице.

```csharp
public string Title { get; set; }
```

### Примечания

Значение по умолчанию — пустая строка.

Это свойство имеет значение для совместимых с ISO/IEC 29500 документов DOCX ([`OoxmlCompliance`](../../../aspose.words.saving/ooxmlcompliance/)). При сохранении в форматах, предшествующих ISO/IEC 29500, это свойство игнорируется.

### Примеры

Показывает, как построить вложенную таблицу без использования построителя документов.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Создадим внешнюю таблицу с тремя строками и четырьмя столбцами, а затем добавим ее в документ.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Создайте еще одну таблицу с двумя строками и двумя столбцами, а затем вставьте ее в первую ячейку первой таблицы.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Создает новую таблицу в документе с заданными размерами и текстом в каждой ячейке.
/// </summary>
private static Table CreateTable(Document doc, int rowCount, int cellCount, string cellText)
{
    Table table = new Table(doc);

    for (int rowId = 1; rowId <= rowCount; rowId++)
    {
        Row row = new Row(doc);
        table.AppendChild(row);

        for (int cellId = 1; cellId <= cellCount; cellId++)
        {
            Cell cell = new Cell(doc);
            cell.AppendChild(new Paragraph(doc));
            cell.FirstParagraph.AppendChild(new Run(doc, cellText));

            row.AppendChild(cell);
        }
    }

    // Вы можете использовать свойства «Заголовок» и «Описание», чтобы добавить заголовок и описание соответственно к вашей таблице.
    // В таблице должна быть хотя бы одна строка, прежде чем мы сможем использовать эти свойства.
    // Эти свойства имеют значение для документов .docx, совместимых с ISO/IEC 29500 (см. класс OoxmlCompliance).
    // Если мы сохраняем документ в форматах, предшествующих ISO/IEC 29500, Microsoft Word игнорирует эти свойства.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Смотрите также

* class [Table](../)
* пространство имен [Aspose.Words.Tables](../../table/)
* сборка [Aspose.Words](../../../)


