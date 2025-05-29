---
title: ShapeBase.GetShapeRenderer
linktitle: GetShapeRenderer
articleTitle: GetShapeRenderer
second_title: Aspose.Words для .NET
description: Откройте для себя метод ShapeBase GetShapeRenderer, позволяющий легко создавать и визуализировать фигуры в виде изображений, с легкостью улучшая ваши дизайн-проекты.
type: docs
weight: 670
url: /ru/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

Создает и возвращает объект, который можно использовать для преобразования этой фигуры в изображение.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### Возвращаемое значение

Объект рендеринга для этой формы.

## Примечания

Этот метод просто вызывает[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) конструктор и передает этот объект в качестве параметра.

## Примеры

Показывает, как использовать средство визуализации фигур для экспорта фигур в файлы в локальной файловой системе.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// В документе 7 фигур, включая одну групповую фигуру с 2 дочерними фигурами.
// Мы отобразим каждую фигуру в файле изображения в локальной файловой системе
// игнорируя при этом групповые фигуры, поскольку они не имеют внешнего вида.
// Это создаст 6 файлов изображений.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Смотрите также

* class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* class [ShapeBase](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
