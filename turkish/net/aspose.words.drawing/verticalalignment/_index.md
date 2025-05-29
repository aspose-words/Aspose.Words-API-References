---
title: VerticalAlignment Enum
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: .NET için Aspose.Words
description: Belgelerinizdeki metin çerçevelerinin ve tabloların hassas dikey hizalaması için Aspose.Words.Drawing.VerticalAlignment enum'unu keşfedin. Düzen kontrolünü geliştirin!
type: docs
weight: 1790
url: /tr/net/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enumeration

Yüzen bir şeklin, metin çerçevesinin veya yüzen bir tablonun dikey hizalamasını belirtir.

```csharp
public enum VerticalAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Nesne, genellikle kendi kullanımıyla açıkça konumlandırılır.**Tepe** mülk. |
| Top | `1` | Nesnenin dikey hizalama tabanının en üstünde olacağını belirtir. |
| Center | `2` | Nesnenin dikey hizalama tabanına göre ortalanması gerektiğini belirtir. |
| Bottom | `3` | Nesnenin dikey hizalama tabanının en altında olacağını belirtir. |
| Inside | `4` | Nesnenin yatay hizalama tabanının içinde olacağını belirtir. |
| Outside | `5` | Nesnenin dikey hizalama tabanının dışında olacağını belirtir. |
| Inline | `-1` | Belgelenmemiş. Yüzen paragraflar ve tablolar için olası bir değer gibi görünüyor. |
| Default | `0` | AynısıNone . |

## Örnekler

Sayfanın ortasına kayan bir resmin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Üst üste gelen metnin arkasında görünecek yüzen bir resim ekleyin ve onu sayfanın ortasına hizalayın.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### Ayrıca bakınız

* property [VerticalAlignment](../shapebase/verticalalignment/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
