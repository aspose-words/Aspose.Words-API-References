---
title: Enum NodeType
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.NodeType перечисление. Указывает тип узла документа Word.
type: docs
weight: 4230
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
| Any | `0` | Указывает все типы узлов. Позволяет выбрать всех детей. |
| Document | `1` | А[`Document`](../document/) объект, который, являясь корнем дерева документов, обеспечивает доступ ко всему документу Word. |
| Section | `2` | А[`Section`](../section/) объект, соответствующий одному разделу документа Word. |
| Body | `3` | А[`Body`](../body/) объект, содержащий основной текст раздела (основной текстовый сюжет). |
| HeaderFooter | `4` | А[`HeaderFooter`](../headerfooter/) объект, содержащий текст определенного верхнего или нижнего колонтитула внутри раздела. |
| Table | `5` | А[`Table`](../../aspose.words.tables/table/) объект, представляющий таблицу в документе Word. |
| Row | `6` | Ряд таблицы. |
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
| Shape | `18` | Объект рисования, например фигура OfficeArt, изображение или объект OLE. |
| Comment | `19` | Комментарий в документе Word. |
| Footnote | `20` | Сноска или концевая сноска в документе Word. |
| Run | `21` | Бег текста. |
| FieldStart | `22` | Специальный символ, обозначающий начало поля Word. |
| FieldSeparator | `23` | Специальный символ, отделяющий код поля от результата поля. |
| FieldEnd | `24` | Специальный символ, обозначающий конец поля Word. |
| FormField | `25` | Поле формы. |
| SpecialChar | `26` | Специальный символ, который не является одним из более конкретных типов специальных символов. |
| SmartTag | `27` | Смарт-тег вокруг одной или нескольких встроенных структур (серий, изображений, полей и т. д.) внутри абзаца. |
| StructuredDocumentTag | `28` | Позволяет определить специфичную для клиента информацию и средства ее представления. |
| StructuredDocumentTagRangeStart | `29` | Начало **дальнего боя** структурированный тег документа, который принимает содержимое из нескольких разделов. |
| StructuredDocumentTagRangeEnd | `30` | Конец **дальнего боя** структурированный тег документа, который принимает содержимое из нескольких разделов. |
| GlossaryDocument | `31` | Документ глоссария внутри основного документа. |
| BuildingBlock | `32` | Строительный блок в документе глоссария (например, запись документа глоссария). |
| CommentRangeStart | `33` | Узел маркера, представляющий начало закомментированного диапазона. |
| CommentRangeEnd | `34` | Узел маркера, представляющий конец закомментированного диапазона. |
| OfficeMath | `35` | Объект Office Math. Может быть уравнением, функцией, матрицей или одним из других математических объектов. Может быть коллекцией математических объектов, а также может содержать некоторые нематематические объекты, такие как фрагменты текста. |
| SubDocument | `36` | Узел вложенного документа, который является ссылкой на другой документ. |
| System | `37` | Зарезервировано для внутреннего использования Aspose.Words. |
| Null | `38` | Зарезервировано для внутреннего использования Aspose.Words. |

### Примеры

Показывает, как перемещаться по коллекции дочерних узлов составного узла.

```csharp
Document doc = new Document();

// Добавьте два прогона и одну фигуру в качестве дочерних узлов в первый абзац этого документа.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Обратите внимание, что CustomNodeId не сохраняется в выходном файле и существует только во время существования узла.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Перебираем коллекцию непосредственных дочерних элементов абзаца,
// и распечатываем любые фрагменты или фигуры, которые мы находим внутри.
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


