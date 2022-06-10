---
title: Table
second_title: Справочник по API Aspose.Words для .NET
description: Представляет таблицу в документе Word.
type: docs
weight: 5990
url: /ru/net/aspose.words.tables/table/
---
## Table class

Представляет таблицу в документе Word.

```csharp
public class Table : CompositeNode
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [Table](table)(DocumentBase) | Инициализирует новый экземпляр класса **Table** . |

## Характеристики

| Имя | Описание |
| --- | --- |
| [AbsoluteHorizontalDistance](../../aspose.words.tables/table/absolutehorizontaldistance) { get; set; } | Получает или задает абсолютную позицию плавающей таблицы по горизонтали, указанную в свойствах таблицы, в пунктах. Значение по умолчанию:0. |
| [AbsoluteVerticalDistance](../../aspose.words.tables/table/absoluteverticaldistance) { get; set; } | Получает или задает абсолютную вертикальную плавающую позицию таблицы, указанную в свойствах таблицы, в пунктах. Значение по умолчанию:0. |
| [Alignment](../../aspose.words.tables/table/alignment) { get; set; } | Указывает, как встроенная таблица выравнивается в документе. |
| [AllowAutoFit](../../aspose.words.tables/table/allowautofit) { get; set; } | Позволяет Microsoft Word и Aspose.Words автоматически изменять размер ячеек в таблице, чтобы они соответствовали их содержимому. |
| [AllowCellSpacing](../../aspose.words.tables/table/allowcellspacing) { get; set; } | Получает или задает параметр «Разрешить интервалы между ячейками». |
| [AllowOverlap](../../aspose.words.tables/table/allowoverlap) { get; } | Определяет, должна ли плавающая таблица позволять другим плавающим объектам в документе перекрывать свои экстенты при отображении. Значение по умолчанию:` true` . |
| [Bidi](../../aspose.words.tables/table/bidi) { get; set; } | Получает или задает, является ли это таблицей с письмом справа налево. |
| [BottomPadding](../../aspose.words.tables/table/bottompadding) { get; set; } | Получает или задает количество места (в пунктах) для добавления под содержимым ячеек. |
| [CellSpacing](../../aspose.words.tables/table/cellspacing) { get; set; } | Получает или задает расстояние (в пунктах) между ячейками. |
| [ChildNodes](../../aspose.words/compositenode/childnodes) { get; } | Получает все непосредственные дочерние узлы данного узла. |
| [Count](../../aspose.words/compositenode/count) { get; } | Получает количество непосредственных потомков этого узла. |
| [CustomNodeId](../../aspose.words/node/customnodeid) { get; set; } | Указывает идентификатор пользовательского узла. |
| [Description](../../aspose.words.tables/table/description) { get; set; } | Получает или задает описание этой таблицы. Обеспечивает альтернативное текстовое представление информации, содержащейся в таблице. |
| [DistanceBottom](../../aspose.words.tables/table/distancebottom) { get; } | Получает расстояние между нижней частью таблицы и окружающим текстом в пунктах. |
| [DistanceLeft](../../aspose.words.tables/table/distanceleft) { get; } | Получает расстояние между левой частью таблицы и окружающим текстом в пунктах. |
| [DistanceRight](../../aspose.words.tables/table/distanceright) { get; } | Получает расстояние между правой частью таблицы и окружающим текстом в пунктах. |
| [DistanceTop](../../aspose.words.tables/table/distancetop) { get; } | Получает расстояние между столешницей и окружающим текстом в пунктах. |
| virtual [Document](../../aspose.words/node/document) { get; } | Получает документ, которому принадлежит данный узел. |
| [FirstChild](../../aspose.words/compositenode/firstchild) { get; } | Получает первый потомок узла. |
| [FirstRow](../../aspose.words.tables/table/firstrow) { get; } | Возвращает первый узел **Row** в таблице. |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes) { get; } | Возвращает true, если у этого узла есть дочерние узлы. |
| [HorizontalAnchor](../../aspose.words.tables/table/horizontalanchor) { get; set; } | Получает базовый объект, из которого должно быть рассчитано горизонтальное позиционирование плавающей таблицы. Значение по умолчанию:Column. |
| override [IsComposite](../../aspose.words/compositenode/iscomposite) { get; } | Возвращает true, так как этот узел может иметь дочерние узлы. |
| [LastChild](../../aspose.words/compositenode/lastchild) { get; } | Получает последний потомок узла. |
| [LastRow](../../aspose.words.tables/table/lastrow) { get; } | Возвращает последний узел **строки** в таблице. |
| [LeftIndent](../../aspose.words.tables/table/leftindent) { get; set; } | Получает или задает значение, представляющее левый отступ таблицы. |
| [LeftPadding](../../aspose.words.tables/table/leftpadding) { get; set; } | Получает или задает количество места (в пунктах), которое добавляется слева от содержимого ячеек. |
| [NextSibling](../../aspose.words/node/nextsibling) { get; } | Получает узел, следующий сразу за этим узлом. |
| override [NodeType](../../aspose.words.tables/table/nodetype) { get; } | Возвращает **NodeType.Table** . |
| [ParentNode](../../aspose.words/node/parentnode) { get; } | Получает непосредственного родителя этого узла. |
| [PreferredWidth](../../aspose.words.tables/table/preferredwidth) { get; set; } | Получает или задает предпочтительную ширину таблицы. |
| [PreviousSibling](../../aspose.words/node/previoussibling) { get; } | Получает узел, непосредственно предшествующий этому узлу. |
| [Range](../../aspose.words/node/range) { get; } | Возвращает объект **Range** , представляющий часть документа, содержащуюся в этом узле. |
| [RelativeHorizontalAlignment](../../aspose.words.tables/table/relativehorizontalalignment) { get; set; } | Получает или задает относительное горизонтальное выравнивание плавающей таблицы. |
| [RelativeVerticalAlignment](../../aspose.words.tables/table/relativeverticalalignment) { get; set; } | Получает или задает относительное вертикальное выравнивание плавающей таблицы. |
| [RightPadding](../../aspose.words.tables/table/rightpadding) { get; set; } | Получает или задает количество места (в пунктах), добавляемого справа от содержимого ячеек. |
| [Rows](../../aspose.words.tables/table/rows) { get; } | Предоставляет типизированный доступ к строкам таблицы. |
| [Style](../../aspose.words.tables/table/style) { get; set; } | Получает или задает стиль таблицы, применяемый к этой таблице. |
| [StyleIdentifier](../../aspose.words.tables/table/styleidentifier) { get; set; } | Получает или задает независимый от языкового стандарта идентификатор стиля таблицы, примененный к этой таблице. |
| [StyleName](../../aspose.words.tables/table/stylename) { get; set; } | Получает или задает имя стиля таблицы, примененного к этой таблице. |
| [StyleOptions](../../aspose.words.tables/table/styleoptions) { get; set; } | Получает или задает битовые флаги, указывающие, как стиль таблицы применяется к этой таблице. |
| [TextWrapping](../../aspose.words.tables/table/textwrapping) { get; set; } | Получает или устанавливает[`TextWrapping`](./textwrapping)для таблицы. |
| [Title](../../aspose.words.tables/table/title) { get; set; } | Получает или устанавливает заголовок этой таблицы. Обеспечивает альтернативное текстовое представление информации, содержащейся в таблице. |
| [TopPadding](../../aspose.words.tables/table/toppadding) { get; set; } | Получает или задает количество места (в пунктах) для добавления над содержимым ячеек. |
| [VerticalAnchor](../../aspose.words.tables/table/verticalanchor) { get; set; } | Получает базовый объект, из которого должно быть рассчитано вертикальное позиционирование плавающей таблицы. Значение по умолчанию:Margin. |

## Методы

| Имя | Описание |
| --- | --- |
| override [Accept](../../aspose.words.tables/table/accept)(DocumentVisitor) | Принимает посетителя. |
| [AppendChild](../../aspose.words/compositenode/appendchild)(Node) | Добавляет указанный узел в конец списка дочерних узлов для этого узла. |
| [AutoFit](../../aspose.words.tables/table/autofit)(AutoFitBehavior) | Изменяет размер таблицы и ячеек в соответствии с заданным поведением автоподбора. |
| [ClearBorders](../../aspose.words.tables/table/clearborders)() | Удаляет все границы таблиц и ячеек в этой таблице. |
| [ClearShading](../../aspose.words.tables/table/clearshading)() | Удаляет все затенение на столе. |
| [Clone](../../aspose.words/node/clone)(bool) | Создает дубликат узла. |
| [ConvertToHorizontallyMergedCells](../../aspose.words.tables/table/converttohorizontallymergedcells)() | Преобразует ячейки, объединенные по горизонтали по ширине, в ячейки, объединенные[`HorizontalMerge`](../cellformat/horizontalmerge). |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator)() | Зарезервировано для системного использования. IXPathNavigable. |
| [EnsureMinimum](../../aspose.words.tables/table/ensureminimum)() | Если в таблице нет строк, создает и добавляет одну **Row** . |
| [GetAncestor](../../aspose.words/node/getancestor)(NodeType) | Получает первого предка указанного[`NodeType`](../../aspose.words/nodetype). |
| [GetAncestor](../../aspose.words/node/getancestor)(Type) | Получает первого предка указанного типа объекта. |
| [GetChild](../../aspose.words/compositenode/getchild)(NodeType, int, bool) | Возвращает N-й дочерний узел, соответствующий указанному типу. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes)(NodeType, bool) | Возвращает динамическую коллекцию дочерних узлов, соответствующих указанному типу. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator)() | Обеспечивает поддержку для каждой итерации стиля над дочерними узлами этого узла. |
| override [GetText](../../aspose.words/compositenode/gettext)() | Получает текст этого узла и всех его потомков. |
| [IndexOf](../../aspose.words/compositenode/indexof)(Node) | Возвращает индекс указанного дочернего узла в массиве дочерних узлов. |
| [InsertAfter](../../aspose.words/compositenode/insertafter)(Node, Node) | Вставляет указанный узел сразу после указанного опорного узла. |
| [InsertBefore](../../aspose.words/compositenode/insertbefore)(Node, Node) | Вставляет указанный узел непосредственно перед указанным ссылочным узлом. |
| [NextPreOrder](../../aspose.words/node/nextpreorder)(Node) | Получает следующий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [PrependChild](../../aspose.words/compositenode/prependchild)(Node) | Добавляет указанный узел в начало списка дочерних узлов для этого узла. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder)(Node) | Получает предыдущий узел в соответствии с алгоритмом обхода дерева предварительного порядка. |
| [Remove](../../aspose.words/node/remove)() | Удаляет себя из родителя. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren)() | Удаляет все дочерние узлы текущего узла. |
| [RemoveChild](../../aspose.words/compositenode/removechild)(Node) | Удаляет указанный дочерний узел. |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags)() | Удаляет все[`SmartTag`](../../aspose.words.markup/smarttag)узлы-потомки текущего узла. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes)(string) | Выбирает список узлов, соответствующих выражению XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode)(string) | Выбирает первый узел, соответствующий выражению XPath. |
| [SetBorder](../../aspose.words.tables/table/setborder)(BorderType, LineStyle, double, Color, bool) | Устанавливает для указанной границы таблицы заданный стиль, ширину и цвет линии. |
| [SetBorders](../../aspose.words.tables/table/setborders)(LineStyle, double, Color) | Устанавливает для всех границ таблицы заданный стиль линии, ширину и цвет. |
| [SetShading](../../aspose.words.tables/table/setshading)(TextureIndex, Color, Color) | Устанавливает затенение на указанные значения для всей таблицы. |
| [ToString](../../aspose.words/node/tostring)(SaveFormat) | Экспортирует содержимое узла в строку в указанном формате. |
| [ToString](../../aspose.words/node/tostring)(SaveOptions) | Экспортирует содержимое узла в строку, используя указанные параметры сохранения. |

### Примечания

**Таблица** является узел уровня блока и может быть потомком классов, производных от **Story** или  **InlineStory** .

**Таблица** может содержать одну или несколько строк узлов.

В минимально допустимой таблице должна быть хотя бы одна строка .

### Примеры

Показывает, как создать таблицу.

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
     // Эти свойства имеют значение для документов .docx, соответствующих стандарту ISO/IEC 29500 (см. класс OoxmlCompliance).
     // Если мы сохраняем документ в форматах, предшествующих ISO/IEC 29500, Microsoft Word игнорирует эти свойства.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

Показывает, как перебирать все таблицы в документе и печатать содержимое каждой ячейки.

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
     // Эти свойства имеют значение для документов .docx, соответствующих стандарту ISO/IEC 29500 (см. класс OoxmlCompliance).
     // Если мы сохраняем документ в форматах, предшествующих ISO/IEC 29500, Microsoft Word игнорирует эти свойства.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

Показывает, как создать форматированную таблицу 2x2.

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
     // Эти свойства имеют значение для документов .docx, соответствующих стандарту ISO/IEC 29500 (см. класс OoxmlCompliance).
     // Если мы сохраняем документ в форматах, предшествующих ISO/IEC 29500, Microsoft Word игнорирует эти свойства.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
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
     // Эти свойства имеют значение для документов .docx, соответствующих стандарту ISO/IEC 29500 (см. класс OoxmlCompliance).
     // Если мы сохраняем документ в форматах, предшествующих ISO/IEC 29500, Microsoft Word игнорирует эти свойства.
    table.Title = "Aspose table title";
    table.Description = "Aspose table description";

    return table;
}
```

### Смотрите также

* class [CompositeNode](../../aspose.words/compositenode)
* namespace [Aspose.Words.Tables](../../aspose.words.tables)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
