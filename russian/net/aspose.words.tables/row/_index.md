---
title: Class Row
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Tables.Row сорт. Представляет строку таблицы.
type: docs
weight: 6310
url: /ru/net/aspose.words.tables/row/
---
## Row class

Представляет строку таблицы.

Чтобы узнать больше, посетите[Работа с таблицами](https://docs.aspose.com/words/net/working-with-tables/) статья документации.

```csharp
public class Row : CompositeNode
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Row](row/)(DocumentBase) | Инициализирует новый экземпляр`Row` класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Cells](../../aspose.words.tables/row/cells/) { get; } | Обеспечивает типизированный доступ к[`Cell`](../cell/) дочерние узлы строки. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, которому принадлежит этот узел. |
| [FirstCell](../../aspose.words.tables/row/firstcell/) { get; } | Возвращает первый[`Cell`](../cell/) в строке. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первого дочернего элемента узла. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возвращает`истинный` если у этого узла есть дочерние узлы. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возвращает`истинный` поскольку этот узел может иметь дочерние узлы. |
| [IsFirstRow](../../aspose.words.tables/row/isfirstrow/) { get; } | True, если это первая строка в таблице; ложь в противном случае. |
| [IsLastRow](../../aspose.words.tables/row/islastrow/) { get; } | True, если это последняя строка в таблице; ложь в противном случае. |
| [LastCell](../../aspose.words.tables/row/lastcell/) { get; } | Возвращает последний[`Cell`](../cell/) в строке. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последнего дочернего узла узла. |
| [NextRow](../../aspose.words.tables/row/nextrow/) { get; } | Получает следующий`Row` узел. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words.tables/row/nodetype/) { get; } | ВозвращаетRow . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [ParentTable](../../aspose.words.tables/row/parenttable/) { get; } | Возвращает непосредственную родительскую таблицу строки. |
| [PreviousRow](../../aspose.words.tables/row/previousrow/) { get; } | Получает предыдущее`Row` узел. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../../aspose.words/range/) объект, представляющий часть документа, содержащуюся в этом узле. |
| [RowFormat](../../aspose.words.tables/row/rowformat/) { get; } | Предоставляет доступ к свойствам форматирования строки. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.tables/row/accept/)(DocumentVisitor) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words.tables/row/acceptend/)(DocumentVisitor) |  |
| override [AcceptStart](../../aspose.words.tables/row/acceptstart/)(DocumentVisitor) |  |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Создает дубликат узла. |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [EnsureMinimum](../../aspose.words.tables/row/ensureminimum/)() | Если`Row` не имеет ячеек, создает и добавляет одну[`Cell`](../cell/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(NodeType) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(NodeType, bool) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words.tables/row/gettext/)() | Получает текст всех ячеек в этой строке, включая символ конца строки. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(T, Node) |  |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(T, Node) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя от родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/)узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(string) | Выбирает первый[`Node`](../../aspose.words/node/) которое соответствует выражению XPath. |
| [ToString](../../aspose.words/node/tostring/)(SaveFormat) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

`Row` может быть только ребенком[`Table`](../table/).

`Row` может содержать один или несколько[`Cell`](../cell/) узлы.

Минимальная допустимая строка должна иметь хотя бы одну[`Cell`](../cell/).

### Примеры

Показывает, как создать таблицу.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Таблицы содержат строки, содержащие ячейки, которые могут иметь абзацы
// с типичными элементами, такими как прогоны, фигуры и даже другие таблицы.
// Вызов метода EnsureMinimum для таблицы гарантирует, что
// в таблице есть хотя бы одна строка, ячейка и абзац.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Добавляем текст к первому вызову в первой строке таблицы.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Показывает, как перебрать все таблицы в документе и распечатать содержимое каждой ячейки.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Мы можем использовать метод ToArray для коллекции строк, чтобы клонировать ее в массив.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Мы можем использовать метод ToArray для коллекции ячеек, чтобы клонировать ее в массив.
        Assert.AreEqual(cells, cells.ToArray());
        Assert.AreNotSame(cells, cells.ToArray());

        for (int k = 0; k < cells.Count; k++)
        {
            string cellText = cells[k].ToString(SaveFormat.Text).Trim();
            Console.WriteLine($"\t\tContents of Cell:{k} = \"{cellText}\"");
        }

        Console.WriteLine($"\tEnd of Row {j}");
    }

    Console.WriteLine($"End of Table {i}\n");
}
```

Показывает, как построить вложенную таблицу без использования построителя документов.

```csharp
public void CreateNestedTable()
{
    Document doc = new Document();

    // Создаем внешнюю таблицу с тремя строками и четырьмя столбцами, а затем добавляем ее в документ.
    Table outerTable = CreateTable(doc, 3, 4, "Outer Table");
    doc.FirstSection.Body.AppendChild(outerTable);

    // Создайте еще одну таблицу с двумя строками и двумя столбцами, а затем вставьте ее в первую ячейку первой таблицы.
    Table innerTable = CreateTable(doc, 2, 2, "Inner Table");
    outerTable.FirstRow.FirstCell.AppendChild(innerTable);

    doc.Save(ArtifactsDir + "Table.CreateNestedTable.docx");
}

/// <summary>
/// Создает в документе новую таблицу с заданными размерами и текстом в каждой ячейке.
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

    // Вы можете использовать свойства «Название» и «Описание», чтобы добавить в таблицу заголовок и описание соответственно.
    // В таблице должна быть хотя бы одна строка, прежде чем мы сможем использовать эти свойства.
    // Эти свойства имеют смысл для документов .docx, соответствующих стандарту ISO/IEC 29500 (см. класс OoxmlCompliance).
    // Если мы сохраним документ в форматах, предшествующих ISO/IEC 29500, Microsoft Word игнорирует эти свойства.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Смотрите также

* class [CompositeNode](../../aspose.words/compositenode/)
* пространство имен [Aspose.Words.Tables](../../aspose.words.tables/)
* сборка [Aspose.Words](../../)


