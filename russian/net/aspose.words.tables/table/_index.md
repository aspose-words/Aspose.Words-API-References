---
title: Table Class
linktitle: Table
articleTitle: Table
second_title: Aspose.Words для .NET
description: Aspose.Words.Tables.Table сорт. Представляет таблицу в документе Word на С#.
type: docs
weight: 6340
url: /ru/net/aspose.words.tables/table/
---
## Table class

Представляет таблицу в документе Word.

Чтобы узнать больше, посетите[Работа с таблицами](https://docs.aspose.com/words/net/working-with-tables/) статья документации.

```csharp
public class Table : CompositeNode
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Table](table/)(*[DocumentBase](../../aspose.words/documentbase/)*) | Инициализирует новый экземпляр`Table` класс. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | Получает или задает абсолютное горизонтальное плавающее положение таблицы, указанное в свойствах таблицы, в точках. Значение по умолчанию — 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | Получает или задает абсолютное вертикальное плавающее положение таблицы, указанное в свойствах таблицы, в точках. Значение по умолчанию — 0. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | Указывает, как встроенная таблица выравнивается в документе. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | Позволяет Microsoft Word и Aspose.Words автоматически изменять размеры ячеек таблицы в соответствии с их содержимым. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | Получает или задает параметр «Разрешить интервал между ячейками». |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | Определяет, должна ли плавающая таблица позволять другим плавающим объектам в документе перекрывать ее экстенты при отображении. Значение по умолчанию:`истинный` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | Получает или устанавливает, является ли это таблица с письмом справа налево. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | Получает или задает объем пространства (в пунктах), добавляемого под содержимым ячеек. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | Получает или задает расстояние (в пунктах) между ячейками. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных дочерних элементов этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | Получает или задает описание этой таблицы. Предоставляет альтернативное текстовое представление информации, содержащейся в таблице. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; set; } | Получает или задает расстояние между нижней частью таблицы и окружающим текстом в пунктах. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; set; } | Получает или задает расстояние между левой частью таблицы и окружающим текстом в пунктах. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; set; } | Получает или задает расстояние между правой частью таблицы и окружающим текстом в пунктах. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; set; } | Получает или задает расстояние между верхом таблицы и окружающим текстом в пунктах. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, которому принадлежит этот узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первого дочернего элемента узла. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | Возвращает первый[`Row`](../row/) узел в таблице. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возвращает`истинный` если у этого узла есть дочерние узлы. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | Получает базовый объект, на основе которого должно рассчитываться горизонтальное положение плавающей таблицы. Значение по умолчанию:Column . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возвращает`истинный` поскольку этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последнего дочернего узла узла. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | Возвращает последний[`Row`](../row/) узел в таблице. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | Получает или задает значение, представляющее левый отступ таблицы. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | Получает или задает объем места (в пунктах), добавляемый слева от содержимого ячеек. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | ВозвращаетTable . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | Получает или задает предпочтительную ширину таблицы. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../../aspose.words/range/) объект, представляющий часть документа, содержащуюся в этом узле. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | Получает или задает относительное горизонтальное выравнивание плавающей таблицы. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | Получает или задает относительное вертикальное выравнивание плавающей таблицы. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | Получает или задает объем места (в пунктах), добавляемый справа от содержимого ячеек. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | Обеспечивает типизированный доступ к строкам таблицы. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | Получает или задает стиль таблицы, примененный к этой таблице. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | Получает или задает независимый от локали идентификатор стиля таблицы, примененный к этой таблице. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | Получает или задает имя стиля таблицы, примененного к этой таблице. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | Получает или устанавливает битовые флаги, определяющие, как стиль таблицы применяется к этой таблице. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | Получает или устанавливает[`TextWrapping`](./textwrapping/) для таблицы. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | Получает или задает заголовок этой таблицы. Он обеспечивает альтернативное текстовое представление информации, содержащейся в таблице. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | Получает или задает объем пространства (в пунктах), добавляемого над содержимым ячеек. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | Получает базовый объект, на основе которого должно рассчитываться вертикальное положение плавающей таблицы. Значение по умолчанию:Margin . |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../../aspose.words/node/)*) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [AutoFit](../../aspose.words.tables/table/autofit/)(*[AutoFitBehavior](../autofitbehavior/)*) | Изменяет размеры таблицы и ячеек в соответствии с указанным поведением автоподбора. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | Удаляет все границы таблиц и ячеек в этой таблице. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | Удаляет всю тень на столе. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | Преобразует ячейки, объединенные горизонтально по ширине, в ячейки, объединенные по ширине.[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | Если в таблице нет строк, создается и добавляется одна[`Row`](../row/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних элементов. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../../aspose.words/node/), [Node](../../aspose.words/node/)*) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../../aspose.words/node/)*) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного заказа. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя от родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../../aspose.words/node/)*) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/)узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Выбирает первый[`Node`](../../aspose.words/node/) которое соответствует выражению XPath. |
| [SetBorder](../../aspose.words.tables/table/setborder/)(*[BorderType](../../aspose.words/bordertype/), [LineStyle](../../aspose.words/linestyle/), double, Color, bool*) | Устанавливает указанную границу таблицы с указанным стилем, шириной и цветом линии. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(*[LineStyle](../../aspose.words/linestyle/), double, Color*) | Устанавливает для всех границ таблицы указанный стиль, ширину и цвет линий. |
| [SetShading](../../aspose.words.tables/table/setshading/)(*[TextureIndex](../../aspose.words/textureindex/), Color, Color*) | Устанавливает затенение на указанные значения для всей таблицы. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

`Table`является узлом уровня блока и может быть дочерним элементом классов, производных от[`Story`](../../aspose.words/story/) или [`InlineStory`](../../aspose.words/inlinestory/).

`Table` может содержать один или несколько[`Row`](../row/) узлы.

Минимальная допустимая таблица должна иметь хотя бы один[`Row`](../row/).

## Примеры

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

Показывает, как построить форматированную таблицу 2x2.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// При построении таблицы построитель документов будет применять текущие значения свойств RowFormat/CellFormat
// к текущей строке/ячейке, в которой находится курсор, и к любым новым строкам/ячейкам по мере их создания.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Ранее добавленные строки и ячейки не имеют обратной силы при изменении форматирования построителя.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
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
