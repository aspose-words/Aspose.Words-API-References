---
title: Cell
linktitle: Cell
articleTitle: Cell
second_title: Aspose.Words для .NET
description: Откройте для себя конструктор Cell, чтобы легко создавать новые экземпляры класса Cell. Оптимизируйте процесс кодирования и повысьте эффективность разработки!
type: docs
weight: 10
url: /ru/net/aspose.words.tables/cell/cell/
---
## Cell constructor

Инициализирует новый экземпляр[`Cell`](../) класс.

```csharp
public Cell(DocumentBase doc)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | DocumentBase | Документ владельца. |

## Примечания

Когда[`Cell`](../) создан, он принадлежит указанному документу, но еще не является частью документа и[`ParentNode`](../../../aspose.words/node/parentnode/) является`нулевой`.

Чтобы добавить[`Cell`](../) к использованию документа[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) или[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) в строке, куда вы хотите вставить ячейку.

## Примеры

Показывает, как построить вложенную таблицу без использования конструктора документов.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Создаем внешнюю таблицу с тремя строками и четырьмя столбцами, а затем добавляем ее в документ.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Создаем еще одну таблицу с двумя строками и двумя столбцами, а затем вставляем ее в первую ячейку первой таблицы.
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

    // Вы можете использовать свойства «Заголовок» и «Описание», чтобы добавить заголовок и описание к вашей таблице соответственно.
    // Таблица должна иметь хотя бы одну строку, прежде чем мы сможем использовать эти свойства.
    // Эти свойства имеют значение для документов .docx, соответствующих стандарту ISO/IEC 29500 (см. класс OoxmlCompliance).
    // Если мы сохраняем документ в форматах, предшествующих ISO/IEC 29500, Microsoft Word игнорирует эти свойства.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Смотрите также

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [Cell](../)
* пространство имен [Aspose.Words.Tables](../../../aspose.words.tables/)
* сборка [Aspose.Words](../../../)
