---
title: Fill.TextureAlignment
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words for .NET
description: Fill TextureAlignment mülk. Döşeme dokusu dolgusunun hizalamasını alır veya ayarlar C#'da.
type: docs
weight: 180
url: /tr/net/aspose.words.drawing/fill/texturealignment/
---
## Fill.TextureAlignment property

Döşeme dokusu dolgusunun hizalamasını alır veya ayarlar.

```csharp
public TextureAlignment TextureAlignment { get; set; }
```

## Örnekler

Şeklin içindeki dokunun nasıl doldurulacağını ve döşeneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Şekil dolgusuna doku hizalaması uygulayın.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// "TextureAlignment" elde etmek istiyorsanız şekli DML kullanarak tanımlamak için uyumluluk seçeneğini kullanın
// belge kaydedildikten sonraki özellik.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);
```

### Ayrıca bakınız

* enum [TextureAlignment](../../texturealignment/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
