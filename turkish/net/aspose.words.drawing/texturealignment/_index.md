---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: .NET için Aspose.Words
description: Hassas doku dolgu hizalaması için Aspose.Words.Drawing.TextureAlignment enum'unu keşfedin. Belge tasarımlarınızı kusursuz döşeme seçenekleriyle geliştirin!
type: docs
weight: 1780
url: /tr/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

Doku dolgusunun döşenmesi için hizalamayı belirtir.

```csharp
public enum TextureAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| TopLeft | `0` | Sol üst doku hizalaması. |
| Top | `1` | Üst doku hizalaması. |
| TopRight | `2` | Sağ üst doku hizalaması. |
| Left | `3` | Sol doku hizalaması. |
| Center | `4` | Orta doku hizalaması. |
| Right | `5` | Sağ doku hizalaması. |
| BottomLeft | `6` | Sol alt doku hizalaması. |
| Bottom | `7` | Alt doku hizalaması. |
| BottomRight | `8` | Sağ alt doku hizalaması. |
| None | `9` | Hiçbir doku hizalaması yok. |

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
