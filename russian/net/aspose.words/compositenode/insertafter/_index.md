---
title: CompositeNode.InsertAfter
linktitle: InsertAfter
articleTitle: InsertAfter
second_title: Aspose.Words для .NET
description: Легко вставляйте узлы с помощью метода CompositeNode InsertAfter, улучшая управление структурой данных и обеспечивая эффективное размещение узлов.
type: docs
weight: 150
url: /ru/net/aspose.words/compositenode/insertafter/
---
## CompositeNode.InsertAfter&lt;T&gt; method

Вставляет указанный узел сразу после указанного ссылочного узла.

```csharp
public T InsertAfter<T>(T newChild, Node refChild)
    where T : Node
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| newChild | T | The[`Node`](../../node/) вставить. |
| refChild | Node | The[`Node`](../../node/) это опорный узел.*newChild* ставится после*refChild*. |

### Возвращаемое значение

Вставленный узел.

## Примечания

Если*refChild* является`нулевой` , вставки*newChild* в начале списка дочерних узлов.

Если*newChild* уже есть в дереве, сначала его удаляют.

Если вставляемый узел был создан из другого документа, следует использовать [`ImportNode`](../../documentbase/importnode/) для импорта узла в текущий документ. Импортированный узел затем можно вставить в текущий документ.

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

Показывает, как добавлять, обновлять и удалять дочерние узлы в коллекции дочерних узлов CompositeNode.

```csharp
Document doc = new Document();

// Пустой документ по умолчанию имеет один абзац.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Составные узлы, такие как наш абзац, могут содержать другие составные и встроенные узлы в качестве дочерних.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Создаем еще три узла запуска.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// Тело документа не будет отображать эти прогоны, пока мы не вставим их в составной узел
// который сам по себе является частью дерева узлов документа, как мы это делали при первом запуске.
// Мы можем определить, где находится текстовое содержимое узлов, которые мы вставляем
// появляется в документе, указывая место вставки относительно другого узла в абзаце.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Вставьте вторую строку в абзац перед первой строкой.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Вставьте третий запуск после первого запуска.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Вставляем первую строку в начало коллекции дочерних узлов абзаца.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// Мы можем изменить содержимое прогона, редактируя и удаляя существующие дочерние узлы.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### Смотрите также

* class [Node](../../node/)
* class [CompositeNode](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
