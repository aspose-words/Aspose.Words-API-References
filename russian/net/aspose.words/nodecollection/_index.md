---
title: Class NodeCollection
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.NodeCollection сорт. Представляет набор узлов определенного типа.
type: docs
weight: 3960
url: /ru/net/aspose.words/nodecollection/
---
## NodeCollection class

Представляет набор узлов определенного типа.

```csharp
public class NodeCollection : IEnumerable<Node>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Получает количество узлов в коллекции. |
| [Item](../../aspose.words/nodecollection/item/) { get; } | Извлекает узел по заданному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(Node) | Добавляет узел в конец коллекции. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Удаляет все узлы из этой коллекции и из документа. |
| [Contains](../../aspose.words/nodecollection/contains/)(Node) | Определяет, находится ли узел в коллекции. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Обеспечивает простую итерацию в стиле foreach по набору узлов. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(Node) | Возвращает отсчитываемый от нуля индекс указанного узла. |
| [Insert](../../aspose.words/nodecollection/insert/)(int, Node) | Вставляет узел в коллекцию по указанному индексу. |
| [Remove](../../aspose.words/nodecollection/remove/)(Node) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int) | Удаляет узел с указанным индексом из коллекции и из документа. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Копирует все узлы из коллекции в новый массив узлов. |

### Примечания

**NodeCollection** не владеет узлами, которые он содержит, скорее, это просто выбор узлов указанного типа, но узлы хранятся в дереве под соответствующими родительскими узлами.

**NodeCollection**поддерживает индексированный доступ, итерацию и предоставляет методы добавления и удаления.

**NodeCollection** коллекция является «живой», т. е. изменения дочерних элементов узла object , из которого она была создана, немедленно отражаются в узлах, возвращаемых **NodeCollection** свойства и методы.

**NodeCollection** возвращается[`GetChildNodes`](../compositenode/getchildnodes/) , а также служит базовым классом для коллекций типизированных узлов, таких как[`SectionCollection`](../sectioncollection/) , [`ParagraphCollection`](../paragraphcollection/) и т.п.

**NodeCollection** может быть «плоским» и содержать только непосредственных потомков узла, из которого он был создан , или он может быть «глубоким» и содержать всех потомков.

### Примеры

Показывает, как заменить все фигуры текстового поля фигурами изображения.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### Смотрите также

* class [Node](../node/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


