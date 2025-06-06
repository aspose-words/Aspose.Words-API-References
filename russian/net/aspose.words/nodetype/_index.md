---
title: NodeType Enum
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.NodeType, чтобы легко определять и управлять различными типами узлов документов Word для бесперебойной обработки документов.
type: docs
weight: 4920
url: /ru/net/aspose.words/nodetype/
---
## NodeType enumeration

Указывает тип узла документа Word.

```csharp
public enum NodeType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Any | `0` | Указывает все типы узлов. Позволяет выбрать всех дочерних элементов. |
| Document | `1` | А[`Document`](../document/) объект, который, являясь корнем дерева документов, обеспечивает доступ ко всему документу Word. |
| Section | `2` | А[`Section`](../section/) объект, соответствующий одному разделу в документе Word. |
| Body | `3` | А[`Body`](../body/) объект, содержащий основной текст раздела (основной текст статьи). |
| HeaderFooter | `4` | А[`HeaderFooter`](../headerfooter/) объект, содержащий текст определенного верхнего или нижнего колонтитула внутри раздела. |
| Table | `5` | А[`Table`](../../aspose.words.tables/table/) объект, представляющий таблицу в документе Word. |
| Row | `6` | Ряд таблиц. |
| Cell | `7` | Ячейка строки таблицы. |
| Paragraph | `8` | Абзац текста. |
| BookmarkStart | `9` | Начало маркера закладки. |
| BookmarkEnd | `10` | Конец маркера закладки. |
| EditableRangeStart | `11` | Начало редактируемого диапазона. |
| EditableRangeEnd | `12` | Конец редактируемого диапазона. |
| MoveFromRangeStart | `13` | Начало диапазона MoveFrom. |
| MoveFromRangeEnd | `14` | Конец диапазона MoveFrom. |
| MoveToRangeStart | `15` | Начало диапазона MoveTo. |
| MoveToRangeEnd | `16` | Конец диапазона MoveTo. |
| GroupShape | `17` | Группа фигур, изображений, объектов OLE или других групповых фигур. |
| Shape | `18` | Объект рисунка, например фигура OfficeArt, изображение или объект OLE. |
| Comment | `19` | Комментарий в документе Word. |
| Footnote | `20` | Сноска или концевая сноска в документе Word. |
| Run | `21` | Текстовый фрагмент. |
| FieldStart | `22` | Специальный символ, обозначающий начало поля Word. |
| FieldSeparator | `23` | Специальный символ, который отделяет код поля от результата поля. |
| FieldEnd | `24` | Специальный символ, обозначающий конец поля Word. |
| FormField | `25` | Поле формы. |
| SpecialChar | `26` | Специальный символ, не входящий в число более специфичных типов специальных символов. |
| SmartTag | `27` | Смарт-тег вокруг одной или нескольких встроенных структур (цепочек, изображений, полей и т. д.) внутри абзаца. |
| StructuredDocumentTag | `28` | Позволяет определить специфичную для клиента информацию и способы ее представления. |
| StructuredDocumentTagRangeStart | `29` | Начало**дальний** структурированный тег документа, который принимает многосекционный контент. |
| StructuredDocumentTagRangeEnd | `30` | Конец**дальний** структурированный тег документа, который принимает многосекционный контент. |
| GlossaryDocument | `31` | Глоссарий в основном документе. |
| BuildingBlock | `32` | Строительный блок в документе глоссария (например, запись документа глоссария). |
| CommentRangeStart | `33` | Узел маркера, представляющий начало прокомментированного диапазона. |
| CommentRangeEnd | `34` | Узел маркера, представляющий конец прокомментированного диапазона. |
| OfficeMath | `35` | Объект Office Math. Может быть уравнением, функцией, матрицей или одним из других математических объектов. Может быть коллекцией математических объектов, а также может содержать некоторые нематематические объекты, такие как фрагменты текста. |
| SubDocument | `36` | Узел поддокумента, являющийся ссылкой на другой документ. |
| System | `37` | Зарезервировано для внутреннего использования Aspose.Words. |
| Null | `38` | Зарезервировано для внутреннего использования Aspose.Words. |

## Примеры

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
