---
title: Table Class
linktitle: Table
articleTitle: Table
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Tables.Table, который позволяет легко создавать и управлять таблицами в документах Word, улучшая структуру и функциональность вашего документа.
type: docs
weight: 7190
url: /ru/net/aspose.words.tables/table/
---
## Table class

Представляет таблицу в документе Word.

Чтобы узнать больше, посетите[Работа с таблицами](https://docs.aspose.com/words/net/working-with-tables/) документальная статья.

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
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance/) { get; set; } | Возвращает или задает абсолютное горизонтальное положение плавающей таблицы, указанное свойствами таблицы, в пунктах. Значение по умолчанию — 0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance/) { get; set; } | Возвращает или задает абсолютное вертикальное положение плавающей таблицы, указанное свойствами таблицы, в пунктах. Значение по умолчанию — 0. |
| [Alignment](../../aspose.words.tables/table/alignment/) { get; set; } | Указывает, как встроенная таблица выравнивается в документе. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit/) { get; set; } | Позволяет Microsoft Word и Aspose.Words автоматически изменять размер ячеек в таблице в соответствии с их содержимым. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing/) { get; set; } | Возвращает или задает параметр «Разрешить интервал между ячейками». |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap/) { get; } | Определяет, должна ли плавающая таблица позволять другим плавающим объектам в документе перекрывать ее экстенты при отображении. Значение по умолчанию:`истинный` . |
| [Bidi](../../aspose.words.tables/table/bidi/) { get; set; } | Возвращает или задает, является ли эта таблица таблицей с направлением справа налево. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding/) { get; set; } | Возвращает или задает размер пространства (в пунктах), добавляемого под содержимым ячеек. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing/) { get; set; } | Возвращает или задает величину пространства (в пунктах) между ячейками. |
| [Count](../../aspose.words/compositenode/count/) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | Указывает пользовательский идентификатор узла. |
| [Description](../../aspose.words.tables/table/description/) { get; set; } | Получает или задает описание этой таблицы. Предоставляет альтернативное текстовое представление информации, содержащейся в таблице. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom/) { get; set; } | Возвращает или задает расстояние между нижней частью таблицы и окружающим текстом в пунктах. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft/) { get; set; } | Возвращает или задает расстояние между левым краем таблицы и окружающим текстом в пунктах. |
| [DistanceRight](../../aspose.words.tables/table/distanceright/) { get; set; } | Возвращает или задает расстояние между правым краем таблицы и окружающим текстом в пунктах. |
| [DistanceTop](../../aspose.words.tables/table/distancetop/) { get; set; } | Возвращает или задает расстояние между верхом таблицы и окружающим текстом в пунктах. |
| virtual [Document](../../aspose.words/node/document/) { get; } | Получает документ, к которому принадлежит этот узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | Получает первый дочерний элемент узла. |
| [FirstRow](../../aspose.words.tables/table/firstrow/) { get; } | Возвращает первый[`Row`](../row/) узел в таблице. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | Возврат`истинный` если у этого узла есть дочерние узлы. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor/) { get; set; } | Получает базовый объект, на основе которого следует рассчитать горизонтальное положение плавающей таблицы. Значение по умолчанию:Column . |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | Возврат`истинный` так как этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | Получает последний дочерний элемент узла. |
| [LastRow](../../aspose.words.tables/table/lastrow/) { get; } | Возвращает последний[`Row`](../row/) узел в таблице. |
| [LeftIndent](../../aspose.words.tables/table/leftindent/) { get; set; } | Возвращает или задает значение, представляющее левый отступ таблицы. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding/) { get; set; } | Возвращает или задает размер пространства (в пунктах), добавляемого слева от содержимого ячеек. |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | Получает узел, следующий сразу за данным узлом. |
| override [NodeType](../../aspose.words.tables/table/nodetype/) { get; } | ВозвратTable . |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | Получает непосредственного родителя этого узла. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth/) { get; set; } | Получает или задает предпочтительную ширину таблицы. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | Получает узел, непосредственно предшествующий данному узлу. |
| [Range](../../aspose.words/node/range/) { get; } | Возвращает[`Range`](../../aspose.words/range/)объект, представляющий часть документа, содержащуюся в этом узле. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment/) { get; set; } | Возвращает или задает относительное горизонтальное выравнивание плавающей таблицы. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment/) { get; set; } | Возвращает или задает относительное вертикальное выравнивание плавающей таблицы. |
| [RightPadding](../../aspose.words.tables/table/rightpadding/) { get; set; } | Возвращает или задает размер пространства (в пунктах), добавляемого справа от содержимого ячеек. |
| [Rows](../../aspose.words.tables/table/rows/) { get; } | Предоставляет типизированный доступ к строкам таблицы. |
| [Style](../../aspose.words.tables/table/style/) { get; set; } | Возвращает или задает стиль таблицы, примененный к этой таблице. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier/) { get; set; } | Возвращает или задает независимый от локали идентификатор стиля таблицы, примененный к этой таблице. |
| [StyleName](../../aspose.words.tables/table/stylename/) { get; set; } | Возвращает или задает имя стиля таблицы, примененного к этой таблице. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions/) { get; set; } | Возвращает или задает битовые флаги, которые определяют, как стиль таблицы применяется к этой таблице. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping/) { get; set; } | Получает или устанавливает[`TextWrapping`](./textwrapping/) для таблицы. |
| [Title](../../aspose.words.tables/table/title/) { get; set; } | Получает или задает заголовок этой таблицы. Предоставляет альтернативное текстовое представление информации, содержащейся в таблице. |
| [TopPadding](../../aspose.words.tables/table/toppadding/) { get; set; } | Возвращает или задает размер пространства (в пунктах), добавляемого над содержимым ячеек. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor/) { get; set; } | Получает базовый объект, на основе которого следует рассчитать вертикальное положение плавающей таблицы. Значение по умолчанию:Margin . |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя. |
| override [AcceptEnd](../../aspose.words.tables/table/acceptend/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя для посещения конца таблицы. |
| override [AcceptStart](../../aspose.words.tables/table/acceptstart/)(*[DocumentVisitor](../../aspose.words/documentvisitor/)*) | Принимает посетителя для посещения начала таблицы. |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | Добавляет указанный узел в конец списка дочерних узлов для данного узла. |
| [AutoFit](../../aspose.words.tables/table/autofit/)(*[AutoFitBehavior](../autofitbehavior/)*) | Изменяет размер таблицы и ячеек в соответствии с указанным поведением автоподбора. |
| [ClearBorders](../../aspose.words.tables/table/clearborders/)() | Удаляет все границы таблиц и ячеек в этой таблице. |
| [ClearShading](../../aspose.words.tables/table/clearshading/)() | Удаляет все затенения на столе. |
| [Clone](../../aspose.words/node/clone/)(*bool*) | Создает дубликат узла. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells/)() | Преобразует ячейки, объединенные по горизонтали по ширине, в ячейки, объединенные по[`HorizontalMerge`](../cellformat/horizontalmerge/) . |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | Создает навигатор, который можно использовать для перемещения и чтения узлов. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum/)() | Если в таблице нет строк, создает и добавляет одну[`Row`](../row/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../../aspose.words/nodetype/)*) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype/) . |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../../aspose.words/nodetype/), int, bool*) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../../aspose.words/nodetype/), bool*) | Возвращает живую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | Обеспечивает поддержку для каждой итерации стиля по дочерним узлам этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext/)() | Получает текст этого узла и всех его дочерних узлов. |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../../aspose.words/node/)*) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../../aspose.words/node/)*) | Вставляет указанный узел сразу после указанного ссылочного узла. |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../../aspose.words/node/)*) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../../aspose.words/node/)*) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | Добавляет указанный узел в начало списка дочерних узлов для данного узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../../aspose.words/node/)*) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove/)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag/) узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | Выбирает первый[`Node`](../../aspose.words/node/) что соответствует выражению XPath. |
| [SetBorder](../../aspose.words.tables/table/setborder/)(*[BorderType](../../aspose.words/bordertype/), [LineStyle](../../aspose.words/linestyle/), double, Color, bool*) | Устанавливает указанную границу таблицы на указанный стиль линии, ширину и цвет. |
| [SetBorders](../../aspose.words.tables/table/setborders/)(*[LineStyle](../../aspose.words/linestyle/), double, Color*) | Устанавливает для всех границ таблицы указанный стиль линии, ширину и цвет. |
| [SetShading](../../aspose.words.tables/table/setshading/)(*[TextureIndex](../../aspose.words/textureindex/), Color, Color*) | Устанавливает затенение для указанных значений по всей таблице. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../../aspose.words/saveformat/)*) | Экспортирует содержимое узла в строку указанного формата. |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

## Примечания

`Table` является узлом блочного уровня и может быть потомком классов, производных от[`Story`](../../aspose.words/story/) или [`InlineStory`](../../aspose.words/inlinestory/).

`Table` может содержать один или несколько[`Row`](../row/) узлы.

Минимально допустимая таблица должна иметь по крайней мере один[`Row`](../row/).

## Примеры

Показывает, как создать таблицу.

```csharp
Document doc = new Document();
Table table = new Table(doc);
doc.FirstSection.Body.AppendChild(table);

// Таблицы содержат строки, которые содержат ячейки, которые могут иметь абзацы
// с типичными элементами, такими как ряды, фигуры и даже другие таблицы.
// Вызов метода "EnsureMinimum" для таблицы гарантирует, что
// таблица имеет как минимум одну строку, ячейку и абзац.
Row firstRow = new Row(doc);
table.AppendChild(firstRow);

Cell firstCell = new Cell(doc);
firstRow.AppendChild(firstCell);

Paragraph paragraph = new Paragraph(doc);
firstCell.AppendChild(paragraph);

// Добавляем текст в первую ячейку первой строки таблицы.
Run run = new Run(doc, "Hello world!");
paragraph.AppendChild(run);

doc.Save(ArtifactsDir + "Table.CreateTable.docx");
```

Показывает, как выполнить итерацию по всем таблицам в документе и распечатать содержимое каждой ячейки.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
TableCollection tables = doc.FirstSection.Body.Tables;

Assert.AreEqual(2, tables.ToArray().Length);

for (int i = 0; i < tables.Count; i++)
{
    Console.WriteLine($"Start of Table {i}");

    RowCollection rows = tables[i].Rows;

    // Мы можем использовать метод «ToArray» для коллекции строк, чтобы клонировать ее в массив.
    Assert.AreEqual(rows, rows.ToArray());
    Assert.AreNotSame(rows, rows.ToArray());

    for (int j = 0; j < rows.Count; j++)
    {
        Console.WriteLine($"\tStart of Row {j}");

        CellCollection cells = rows[j].Cells;

        // Мы можем использовать метод «ToArray» для коллекции ячеек, чтобы клонировать ее в массив.
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

Показывает, как построить отформатированную таблицу 2x2.

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

// При построении таблицы конструктор документов применит текущие значения свойств RowFormat/CellFormat
// к текущей строке/ячейке, в которой находится курсор, и ко всем новым строкам/ячейкам по мере их создания.
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

// Изменения в форматировании конструктора не влияют на ранее добавленные строки и ячейки.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

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

* class [CompositeNode](../../aspose.words/compositenode/)
* пространство имен [Aspose.Words.Tables](../../aspose.words.tables/)
* сборка [Aspose.Words](../../)
