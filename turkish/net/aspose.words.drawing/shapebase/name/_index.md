---
title: ShapeBase.Name
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. İsteğe bağlı şekil adını alır veya ayarlar.
type: docs
weight: 400
url: /tr/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

İsteğe bağlı şekil adını alır veya ayarlar.

```csharp
public string Name { get; set; }
```

### Notlar

Varsayılan boş dizedir.

Olamaz`hükümsüz`, ancak boş bir dize olabilir.

### Örnekler

Bir şeklin alternatif metninin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Bir şeklin alternatif metnine sağ tıklayarak ve ardından "Otomatik Şekil Biçimlendir" -> aracılığıyla erişebiliriz. "Alternatif Metin".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Belgeyi HTML'ye kaydedin ve ardından şeklimize ait bağlantılı görüntüyü silin.
// HTML'mizi okuyan tarayıcı, eksik görselin yerine alternatif metni görüntüleyecektir.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


