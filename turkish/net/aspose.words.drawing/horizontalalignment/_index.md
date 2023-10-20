---
title: HorizontalAlignment Enum
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words for .NET
description: Aspose.Words.Drawing.HorizontalAlignment Sıralama. Kayan bir şeklin metin çerçevesinin veya kayan tablonun yatay hizalamasını belirtir C#'da.
type: docs
weight: 1030
url: /tr/net/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enumeration

Kayan bir şeklin, metin çerçevesinin veya kayan tablonun yatay hizalamasını belirtir.

```csharp
public enum HorizontalAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Nesne, genellikle kendi özelliği kullanılarak açıkça konumlandırılır.**Sol** özellik. |
| Default | `0` | Şununla aynıNone . |
| Left | `1` | Nesnenin yatay hizalama tabanına göre sola hizalanacağını belirtir. |
| Center | `2` | Nesnenin yatay hizalama tabanına göre ortalanacağını belirtir. |
| Right | `3` | Nesnenin yatay hizalama tabanına doğru hizalanacağını belirtir. |
| Inside | `4` | Nesnenin yatay hizalama tabanının içinde olacağını belirtir. |
| Outside | `5` | Nesnenin yatay hizalama tabanının dışında olacağını belirtir. |

## Örnekler

Sayfanın ortasına kayan bir görüntünün nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Çakışan metnin arkasında görünecek kayan bir resim ekleyin ve onu sayfanın ortasına hizalayın.
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
