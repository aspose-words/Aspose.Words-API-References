---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: .NET için Aspose.Words
description: Döşeme doku dolgusunu optimize etmek için TextureAlignment özelliğini ayarlayın. Gelişmiş görsel çekicilik ve tasarım hassasiyeti için hizalamayı kolayca özelleştirin.
type: docs
weight: 190
url: /tr/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Döşeme doku dolgusu için hizalamayı alır veya ayarlar.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

## Örnekler

Şeklin içindeki dokuyu nasıl dolduracağınızı ve döşeyeceğinizi gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Şekil dolgusuna doku hizalamasını uygula.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// "TextureAlignment" elde etmek istiyorsanız, DML kullanarak şekli tanımlamak için uyumluluk seçeneğini kullanın
// belge kaydedildikten sonra özellik.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);

doc = new Document(ArtifactsDir + "Shape.TextureFill.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(TextureAlignment.TopRight, shape.Fill.TextureAlignment);
Assert.AreEqual(PresetTexture.Canvas, shape.Fill.PresetTexture);
```

### Ayrıca bakınız

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
