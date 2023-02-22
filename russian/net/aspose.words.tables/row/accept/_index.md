---
title: Row.Accept
second_title: Справочник по API Aspose.Words для .NET
description: Row метод. Принимает посетителя.
type: docs
weight: 100
url: /ru/net/aspose.words.tables/row/accept/
---
## Row.Accept method

Принимает посетителя.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | DocumentVisitor | Посетитель, который будет посещать узлы. |

### Возвращаемое значение

Истинно, если все узлы были посещены; false, если DocumentVisitor остановил операцию перед посещением всех узлов.

### Примечания

Перечисляет этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод в DocumentVisitor.

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

Вызывает DocumentVisitor.VisitRowStart, затем вызывает Accept для всех дочерних узлов section и вызывает DocumentVisitor.VisitRowEnd в конце.

### Примеры

Показывает, как распечатать структуру узлов каждой таблицы в документе.

```csharp
public void TableToText()
{
    Document doc = new Document(MyDir + "DocumentVisitor-compatible features.docx");
    TableStructurePrinter visitor = new TableStructurePrinter();

    // Когда составной узел принимает посетителя документа, посетитель посещает принимающий узел,
    // а затем обходит все дочерние элементы узла в порядке глубины.
    // Посетитель может читать и изменять каждый посещаемый узел.
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Обходит небинарное дерево дочерних узлов узла.
/// Создает карту в виде строки всех встреченных узлов таблицы и их дочерних элементов.
/// </summary>
public class TableStructurePrinter : DocumentVisitor
{
    public TableStructurePrinter()
    {
        mVisitedTables = new StringBuilder();
        mVisitorIsInsideTable = false;
    }

    public string GetText()
    {
        return mVisitedTables.ToString();
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Run.
    /// Прогоны вне таблиц не записываются.
    /// </summary>
    public override VisitorAction VisitRun(Run run)
    {
        if (mVisitorIsInsideTable) IndentAndAppendLine("[Run] \"" + run.GetText() + "\"");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается таблица.
    /// </summary>
    public override VisitorAction VisitTableStart(Table table)
    {
        int rows = 0;
        int columns = 0;

        if (table.Rows.Count > 0)
        {
            rows = table.Rows.Count;
            columns = table.FirstRow.Count;
        }

        IndentAndAppendLine("[Table start] Size: " + rows + "x" + columns);
        mDocTraversalDepth++;
        mVisitorIsInsideTable = true;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла Table.
    /// </summary>
    public override VisitorAction VisitTableEnd(Table table)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Table end]");
        mVisitorIsInsideTable = false;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Row.
    /// </summary>
    public override VisitorAction VisitRowStart(Row row)
    {
        string rowContents = row.GetText().TrimEnd(new []{ '\u0007', ' ' }).Replace("\u0007", ", ");
        int rowWidth = row.IndexOf(row.LastCell) + 1;
        int rowIndex = row.ParentTable.IndexOf(row);
        string rowStatusInTable = row.IsFirstRow && row.IsLastRow ? "only" : row.IsFirstRow ? "first" : row.IsLastRow ? "last" : "";
        if (rowStatusInTable != "")
        {
            rowStatusInTable = $", the {rowStatusInTable} row in this table,";
        }

        IndentAndAppendLine($"[Row start] Row #{++rowIndex}{rowStatusInTable} width {rowWidth}, \"{rowContents}\"");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла Row.
    /// </summary>
    public override VisitorAction VisitRowEnd(Row row)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Row end]");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда в документе встречается узел Cell.
    /// </summary>
    public override VisitorAction VisitCellStart(Cell cell)
    {
        Row row = cell.ParentRow;
        Table table = row.ParentTable;
        string cellStatusInRow = cell.IsFirstCell && cell.IsLastCell ? "only" : cell.IsFirstCell ? "first" : cell.IsLastCell ? "last" : "";
        if (cellStatusInRow != "")
        {
            cellStatusInRow = $", the {cellStatusInRow} cell in this row";
        }

        IndentAndAppendLine($"[Cell start] Row {table.IndexOf(row) + 1}, Col {row.IndexOf(cell) + 1}{cellStatusInRow}");
        mDocTraversalDepth++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается после посещения всех дочерних узлов узла Cell.
    /// </summary>
    public override VisitorAction VisitCellEnd(Cell cell)
    {
        mDocTraversalDepth--;
        IndentAndAppendLine("[Cell end]");
        return VisitorAction.Continue;
    }

    /// <summary>
    /// Добавляем строку в StringBuilder и делаем отступ в зависимости от того, насколько глубоко находится посетитель
    /// в дерево дочерних узлов текущей таблицы.
    /// </summary>
    /// <param name="text"></param>
    private void IndentAndAppendLine(string text)
    {
        for (int i = 0; i < mDocTraversalDepth; i++)
        {
            mVisitedTables.Append("|  ");
        }

        mVisitedTables.AppendLine(text);
    }

    private bool mVisitorIsInsideTable;
    private int mDocTraversalDepth;
    private readonly StringBuilder mVisitedTables;
}
```

### Смотрите также

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [Row](../)
* пространство имен [Aspose.Words.Tables](../../row/)
* сборка [Aspose.Words](../../../)


