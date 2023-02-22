---
title: GraphicsQualityOptions.UseTileFlipMode
second_title: Справочник по API Aspose.Words для .NET
description: GraphicsQualityOptions свойство. Получает или устанавливает флаг указывающий является ли WrapMode TileFlipXY.
type: docs
weight: 80
url: /ru/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

Получает или устанавливает флаг, указывающий, является ли WrapMode TileFlipXY.

```csharp
public bool UseTileFlipMode { get; set; }
```

### Примечания

WrapMode указывает, как текстура или градиент укладываются плиткой, когда она меньше , чем заполняемая область.

По умолчанию используетTile (указывает плитку без переворачивания). Это вызывает неточную визуализацию масштабированного изображения (с высоким разрешением).

Это свойство позволяет переключить WrapMode наTileFlipXY (указывает, что плитки переворачиваются на по горизонтали при перемещении по строке и переворачиваются по вертикали при перемещении по столбцу).

### Примеры

Показывает, как предотвратить появление белой линии при рендеринге с высоким разрешением.

```csharp
Document doc = new Document(MyDir + "Shape high dpi.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShapeRenderer renderer = shape.GetShapeRenderer();

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png)
{
    Resolution = 500, GraphicsQualityOptions = new GraphicsQualityOptions { UseTileFlipMode = true }
};
renderer.Save(ArtifactsDir + "ImageSaveOptions.UseTileFlipMode.png", saveOptions);
```

### Смотрите также

* class [GraphicsQualityOptions](../)
* пространство имен [Aspose.Words.Saving](../../graphicsqualityoptions/)
* сборка [Aspose.Words](../../../)


