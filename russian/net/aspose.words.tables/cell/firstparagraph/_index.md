---
title: Cell.FirstParagraph
second_title: Справочник по API Aspose.Words для .NET
description: Cell свойство. Получает первый абзац среди непосредственных дочерних элементов.
type: docs
weight: 30
url: /ru/net/aspose.words.tables/cell/firstparagraph/
---
## Cell.FirstParagraph property

Получает первый абзац среди непосредственных дочерних элементов.

```csharp
public Paragraph FirstParagraph { get; }
```

### Примеры

Показывает, как создать вложенную таблицу с помощью построителя документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Строим внешнюю таблицу.
Cell cell = builder.InsertCell();
builder.Writeln("Outer Table Cell 1");
builder.InsertCell();
builder.Writeln("Outer Table Cell 2");
builder.EndTable();

// Переход к первой ячейке внешней таблицы, построение другой таблицы внутри ячейки.
builder.MoveTo(cell.FirstParagraph);
builder.InsertCell();
builder.Writeln("Inner Table Cell 1");
builder.InsertCell();
builder.Writeln("Inner Table Cell 2");
builder.EndTable();

doc.Save(ArtifactsDir + "DocumentBuilder.InsertNestedTable.docx");
```

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Cell](../)
* пространство имен [Aspose.Words.Tables](../../cell/)
* сборка [Aspose.Words](../../../)


