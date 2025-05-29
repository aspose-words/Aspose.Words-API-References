---
title: HorizontalAlignment Enum
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: .NET için Aspose.Words
description: Kayan metin çerçevelerinde ve tablolarda yatay hizalama üzerinde hassas kontrol için Aspose.Words.Drawing.HorizontalAlignment enumunu keşfedin. Belge düzeninizi geliştirin!
type: docs
weight: 1360
url: /tr/net/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enumeration

Yüzen bir şeklin, metin çerçevesinin veya yüzen tablonun yatay hizalamasını belirtir.

```csharp
public enum HorizontalAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Nesne, genellikle kendi kullanımıyla açıkça konumlandırılır.**Sol** mülk. |
| Default | `0` | AynısıNone . |
| Left | `1` | Nesnenin yatay hizalama tabanına göre sola hizalanacağını belirtir. |
| Center | `2` | Nesnenin yatay hizalama tabanına göre ortalanması gerektiğini belirtir. |
| Right | `3` | Nesnenin yatay hizalama tabanına göre sağa hizalanması gerektiğini belirtir. |
| Inside | `4` | Nesnenin yatay hizalama tabanının içinde olacağını belirtir. |
| Outside | `5` | Nesnenin yatay hizalama tabanının dışında olacağını belirtir. |

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

* property [HorizontalAlignment](../shapebase/horizontalalignment/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
