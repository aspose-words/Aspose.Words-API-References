---
title: Fill.PresetTexture
linktitle: PresetTexture
articleTitle: PresetTexture
second_title: .NET için Aspose.Words
description: PresetTexture özelliğini zahmetsizce nasıl ayarlayacağınızı ve tasarımlarınızı çarpıcı dolgu seçenekleriyle nasıl geliştireceğinizi keşfedin. Bugün yaratıcı potansiyelinizi açığa çıkarın!
type: docs
weight: 170
url: /tr/net/aspose.words.drawing/fill/presettexture/
---
## Fill.PresetTexture property

Bir tane alır[`PresetTexture`](../../presettexture/) dolgu için.

```csharp
public PresetTexture PresetTexture { get; }
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

* enum [PresetTexture](../../presettexture/)
* class [Fill](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
