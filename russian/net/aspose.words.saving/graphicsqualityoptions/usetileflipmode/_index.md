---
title: GraphicsQualityOptions.UseTileFlipMode
linktitle: UseTileFlipMode
articleTitle: UseTileFlipMode
second_title: Aspose.Words для .NET
description: GraphicsQualityOptions UseTileFlipMode свойство. Получает или задает флаг указывающий является ли WrapMode значением TileFlipXY на С#.
type: docs
weight: 80
url: /ru/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

Получает или задает флаг, указывающий, является ли WrapMode значением TileFlipXY.

```csharp
public bool UseTileFlipMode { get; set; }
```

## Примечания

WrapMode определяет, как текстура или градиент будет располагаться плиткой, если она меньше , чем заполняемая область.

По умолчанию используетTile (указывает мозаику без переворачивания). Это приводит к неточной визуализации масштабированного изображения (с высоким разрешением).

Это свойство позволяет переключить WrapMode наTileFlipXY (указывает, что плитки переворачиваются на по горизонтали при перемещении по строке и переворачиваются по вертикали при перемещении по столбцу).

## Примеры

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
* пространство имен [Aspose.Words.Saving](../../../aspose.words.saving/)
* сборка [Aspose.Words](../../../)
