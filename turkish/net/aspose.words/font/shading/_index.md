---
title: Font.Shading
linktitle: Shading
articleTitle: Shading
second_title: .NET için Aspose.Words
description: Metninizin görsel çekiciliğini artıran özelleştirilebilir yazı tipi biçimlendirmesi için Gölgeleme nesnesi sağlayan Font Gölgeleme özelliğini keşfedin.
type: docs
weight: 330
url: /tr/net/aspose.words/font/shading/
---
## Font.Shading property

Bir[`Shading`](../../shading/) yazı tipinin gölgelendirme biçimlendirmesine başvuran nesne.

```csharp
public Shading Shading { get; }
```

## Örnekler

Bir belge oluşturucu tarafından oluşturulan metne gölgelendirmenin nasıl uygulanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// Beyaz yazı tipi rengimizi kullanarak oluşturduğumuz metni görünür hale getirmenin bir yolu
// arka plana gölgelendirme efekti uygulamaktır.
Shading shading = builder.Font.Shading;
shading.Texture = TextureIndex.TextureDiagonalUp;
shading.BackgroundPatternColor = Color.OrangeRed;
shading.ForegroundPatternColor = Color.DarkBlue;

builder.Writeln("White text on an orange background with a two-tone texture.");

doc.Save(ArtifactsDir + "Font.Shading.docx");
```

### Ayrıca bakınız

* class [Shading](../../shading/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
