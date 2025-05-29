---
title: NodeCollection Class
linktitle: NodeCollection
articleTitle: NodeCollection
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.NodeCollection, ваше решение для эффективного управления различными типами узлов при обработке документов. Улучшите свой рабочий процесс сегодня!
type: docs
weight: 4890
url: /ru/net/aspose.words/nodecollection/
---
## NodeCollection class

Представляет собой набор узлов определенного типа.

Чтобы узнать больше, посетите[Объектная модель документа Aspose.Words (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/) документальная статья.

```csharp
public class NodeCollection : IEnumerable<Node>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Получает количество узлов в коллекции. |
| [Item](../../aspose.words/nodecollection/item/) { get; } | Извлекает узел по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Добавляет узел в конец коллекции. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Удаляет все узлы из этой коллекции и из документа. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Определяет, находится ли узел в коллекции. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Обеспечивает простую итерацию в стиле «foreach» по коллекции узлов. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Возвращает индекс указанного узла, отсчитываемый от нуля. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Вставляет узел в коллекцию по указанному индексу. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Удаляет узел с указанным индексом из коллекции и из документа. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Копирует все узлы из коллекции в новый массив узлов. |

## Примечания

`NodeCollection` не владеет узлами, которые он содержит, а представляет собой просто выборку nodes указанного типа, но узлы хранятся в дереве под соответствующими родительскими узлами.

`NodeCollection` поддерживает индексированный доступ, итерацию и предоставляет методы добавления и удаления.

The`NodeCollection` Коллекция является «живой», т.е. изменения в дочерних элементах узла object , из которого она была создана, немедленно отражаются в узлах, возвращаемых функцией`NodeCollection` свойства и методы.

`NodeCollection` возвращается[`GetChildNodes`](../compositenode/getchildnodes/) , а также служит базовым классом для типизированных коллекций узлов, таких как[`SectionCollection`](../sectioncollection/) , [`ParagraphCollection`](../paragraphcollection/) и т. д.

`NodeCollection`может быть «плоским» и содержать только непосредственные дочерние элементы узла, из которого он был создан , или он может быть «глубоким» и содержать всех дочерних элементов.

## Примеры

Показывает, как заменить все фигуры текстовых полей фигурами изображений.

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
