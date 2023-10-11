---
title: Enum VerticalAlignment
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.VerticalAlignment Sıralama. Kayan bir şeklin metin çerçevesinin veya kayan bir tablonun dikey hizalamasını belirtir.
type: docs
weight: 1380
url: /tr/net/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enumeration

Kayan bir şeklin, metin çerçevesinin veya kayan bir tablonun dikey hizalamasını belirtir.

```csharp
public enum VerticalAlignment
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Nesne, genellikle kendi özelliği kullanılarak açıkça konumlandırılır. **Tepe** özellik. |
| Top | `1` | Nesnenin dikey hizalama tabanının üstünde olacağını belirtir. |
| Center | `2` | Nesnenin dikey hizalama tabanına göre ortalanacağını belirtir. |
| Bottom | `3` | Nesnenin dikey hizalama tabanının altında olacağını belirtir. |
| Inside | `4` | Nesnenin yatay hizalama tabanının içinde olacağını belirtir. |
| Outside | `5` | Nesnenin dikey hizalama tabanının dışında olacağını belirtir. |
| Inline | `-1` | Belgelenmedi. Kayan paragraflar ve tablolar için olası bir değer gibi görünüyor. |
| Default | `0` | Şununla aynıNone . |

### Örnekler

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

* property [VerticalAlignment](../shapebase/verticalalignment/)
* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)


