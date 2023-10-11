---
title: ShapeBase.GetShapeRenderer
second_title: Справочник по API Aspose.Words для .NET
description: ShapeBase метод. Создает и возвращает объект который можно использовать для рендеринга этой фигуры в изображение.
type: docs
weight: 660
url: /ru/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

Создает и возвращает объект, который можно использовать для рендеринга этой фигуры в изображение.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### Возвращаемое значение

Объект рендеринга для этой фигуры.

### Примечания

Этот метод просто вызывает[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) конструктор и передает этот объект в качестве параметра.

### Примеры

Показывает, как использовать средство рендеринга фигур для экспорта фигур в файлы в локальной файловой системе.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// В документе 7 фигур, включая одну групповую фигуру с двумя дочерними фигурами.
// Мы преобразуем каждую фигуру в файл изображения в локальной файловой системе
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
* пространство имен [Aspose.Words.Drawing](../../shapebase/)
* сборка [Aspose.Words](../../../)


