---
title: ShapeBase.Name
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. İsteğe bağlı şekil adını alır veya ayarlar.
type: docs
weight: 380
url: /tr/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

İsteğe bağlı şekil adını alır veya ayarlar.

```csharp
public string Name { get; set; }
```

### Notlar

Varsayılan boş dizedir.

Null olamaz, ancak boş bir dize olabilir.

### Örnekler

Bir şeklin alternatif metninin nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Bir şeklin alternatif metnine sağ tıklayarak ve ardından "Otomatik Şekil Biçimlendir" -> "Alt Metin".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Belgeyi HTML'ye kaydedin ve ardından şeklimize ait bağlantılı resmi silin.
// HTML'mizi okuyan tarayıcı, eksik resmin yerine alternatif metni görüntüleyecektir.
doc.Save(ArtifactsDir + "Shape.AltText.html");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


