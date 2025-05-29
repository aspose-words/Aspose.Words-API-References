---
title: GraphicsQualityOptions.UseTileFlipMode
linktitle: UseTileFlipMode
articleTitle: UseTileFlipMode
second_title: Aspose.Words для .NET
description: Откройте для себя свойство GraphicsQualityOptions UseTileFlipMode для управления настройками WrapMode с целью повышения визуального качества ваших приложений.
type: docs
weight: 80
url: /ru/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

Возвращает или задает флаг, указывающий, является ли WrapMode TileFlipXY.

```csharp
public bool UseTileFlipMode { get; set; }
```

## Примечания

TheWrapMode определяет, как будет накладываться текстура или градиент, если он меньше заполняемой области на x000d.

По умолчанию используетсяTile (задает мозаичное размещение без отражения). Это приводит к неточной визуализации масштабированного изображения (с высоким разрешением).

Это свойство позволяет переключить WrapMode наTileFlipXY (указывает, что плитки переворачиваются по горизонтали при перемещении по строке и переворачиваются по вертикали при перемещении по столбцу).

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
