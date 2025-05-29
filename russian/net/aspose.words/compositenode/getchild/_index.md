---
title: CompositeNode.GetChild
linktitle: GetChild
articleTitle: GetChild
second_title: Aspose.Words для .NET
description: Откройте для себя метод CompositeNode GetChild, позволяющий легко извлекать N-й дочерний узел определенного типа и повышать эффективность управления данными.
type: docs
weight: 100
url: /ru/net/aspose.words/compositenode/getchild/
---
## CompositeNode.GetChild method

Возвращает N-й дочерний узел, соответствующий указанному типу.

```csharp
public Node GetChild(NodeType nodeType, int index, bool isDeep)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | NodeType | Указывает тип дочернего узла. |
| index | Int32 | Индекс дочернего узла для выбора, начинающийся с нуля. Отрицательные индексы также допускаются и указывают на доступ с конца, , то есть -1, означает последний узел. |
| isDeep | Boolean | `истинный` для рекурсивного выбора из всех дочерних узлов; `ЛОЖЬ` для выбора только среди непосредственных потомков. Смотрите примечания для получения дополнительной информации. |

### Возвращаемое значение

Дочерний узел, который соответствует критериям или`нулевой` если соответствующий узел не найден.

## Примечания

Если индекс выходит за пределы диапазона,`нулевой` возвращается.

Обратите внимание, что узлы разметки (StructuredDocumentTag иSmartTag ) пройдены даже тогда, когда*isDeep* =`ЛОЖЬ` и`GetChild` вызывается для типа узла без разметки. Например, если первый запуск в para обернут в[`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) , он все равно будет возвращен`GetChild`(Run , 0,`ЛОЖЬ`).

## Примеры

Показывает, как применить свойства стиля таблицы непосредственно к элементам таблицы.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// Этот метод касается свойств стиля таблицы, таких как те, которые мы установили выше.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

Показывает, как проходить по коллекции дочерних узлов составного узла.

```csharp
Document doc = new Document();

// Добавьте две трассы и одну форму в качестве дочерних узлов в первый абзац этого документа.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Обратите внимание, что «CustomNodeId» не сохраняется в выходном файле и существует только в течение срока службы узла.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Проходим по коллекции непосредственных дочерних элементов абзаца,
// и распечатать любые найденные нами фрагменты или формы.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, false).Count);

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

### Смотрите также

* class [Node](../../node/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
