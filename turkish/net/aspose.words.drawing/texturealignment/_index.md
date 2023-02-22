---
title: Enum TextureAlignment
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.TextureAlignment Sıralama. Doku dolgusunun döşenmesi için hizalamayı belirtir.
type: docs
weight: 1220
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
| None | `9` | Doku hizalaması yok. |

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)


