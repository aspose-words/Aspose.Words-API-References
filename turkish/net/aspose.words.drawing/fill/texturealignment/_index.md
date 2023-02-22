---
title: Fill.TextureAlignment
second_title: Aspose.Words for .NET API Referansı
description: Fill mülk. Döşeme dokusu dolgusu için hizalamayı alır veya ayarlar.
type: docs
weight: 130
url: /tr/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Döşeme dokusu dolgusu için hizalamayı alır veya ayarlar.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

### Örnekler

Şeklin içindeki dokunun nasıl doldurulacağını ve döşeneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Şekil dolgusuna doku hizalaması uygulayın.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// "TextureAlignment" almak istiyorsanız DML kullanarak şekli tanımlamak için uyumluluk seçeneğini kullanın
// belge kaydedildikten sonra özellik.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);
```

### Ayrıca bakınız

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../fill/)
* toplantı [Aspose.Words](../../../)


