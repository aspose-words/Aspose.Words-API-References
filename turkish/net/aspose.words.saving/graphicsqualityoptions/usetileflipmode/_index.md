---
title: GraphicsQualityOptions.UseTileFlipMode
linktitle: UseTileFlipMode
articleTitle: UseTileFlipMode
second_title: .NET için Aspose.Words
description: Uygulamalarınızda gelişmiş görsel kalite için WrapMode ayarlarını kontrol etmek üzere GraphicsQualityOptions UseTileFlipMode özelliğini keşfedin.
type: docs
weight: 80
url: /tr/net/aspose.words.saving/graphicsqualityoptions/usetileflipmode/
---
## GraphicsQualityOptions.UseTileFlipMode property

WrapMode'un TileFlipXY olup olmadığını belirten bir bayrak alır veya ayarlar.

```csharp
public bool UseTileFlipMode { get; set; }
```

## Notlar

TheWrapMode Doldurulacak alandan x000d daha küçük olduğunda bir doku veya degradenin nasıl döşeneceğini belirtir.

Varsayılan olarak kullanırTile (çevirmeden döşemeyi belirtir). Bu, ölçeklenmiş görüntünün (yüksek çözünürlükte) yanlış işlenmesine neden olur.

Bu özellik, WrapMode'u şu şekilde değiştirmenize olanak tanır:TileFlipXY (bir satır boyunca hareket ettiğinizde fayansların yatay olarak , bir sütun boyunca hareket ettiğinizde ise dikey olarak çevrileceğini belirtir).

## Örnekler

Yüksek çözünürlükte render alırken beyaz çizginin nasıl önleneceğini gösterir.

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

### Ayrıca bakınız

* class [GraphicsQualityOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
