---
title: ShapeBase.AlternativeText
linktitle: AlternativeText
articleTitle: AlternativeText
second_title: .NET için Aspose.Words
description: Grafikler için açıklayıcı metin sağlayarak erişilebilirliği artıran, kullanıcı deneyimini ve SEO'yu iyileştiren ShapeBase AlternativeText özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

Grafik yerine görüntülenecek alternatif metni tanımlar.

```csharp
public string AlternativeText { get; set; }
```

## Notlar

Varsayılan değer boş bir dizedir.

## Örnekler

Bir şeklin alternatif metninin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Şeklin alternatif metnine, şeklin üzerine sağ tıklayıp, "Otomatik Şekli Biçimlendir" -> "Alternatif Metin" yoluyla ulaşabiliriz.
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Belgeyi HTML'e kaydedip, şeklimize ait bağlantılı resmi silelim.
// HTML kodumuzu okuyan tarayıcı, eksik görselin yerine alternatif metni görüntüleyecektir.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
