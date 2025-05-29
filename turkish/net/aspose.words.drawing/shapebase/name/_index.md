---
title: ShapeBase.Name
linktitle: Name
articleTitle: Name
second_title: .NET için Aspose.Words
description: İsteğe bağlı şekil adlarını kolayca yönetmek, tasarım esnekliğinizi ve proje organizasyonunuzu geliştirmek için ShapeBase Name özelliğini keşfedin.
type: docs
weight: 420
url: /tr/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

İsteğe bağlı şekil adını alır veya ayarlar.

```csharp
public string Name { get; set; }
```

## Notlar

Varsayılan boş dizgedir.

Olamaz`hükümsüz`, ancak boş bir dize de olabilir.

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
