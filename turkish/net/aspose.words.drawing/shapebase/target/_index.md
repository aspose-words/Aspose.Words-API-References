---
title: ShapeBase.Target
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Şekil köprüsü için hedef çerçeveyi alır veya ayarlar.
type: docs
weight: 520
url: /tr/net/aspose.words.drawing/shapebase/target/
---
## ShapeBase.Target property

Şekil köprüsü için hedef çerçeveyi alır veya ayarlar.

```csharp
public string Target { get; set; }
```

### Notlar

Varsayılan değer boş bir dizedir.

### Örnekler

Görüntü içeren ve aynı zamanda köprü olan bir şeklin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + Microsoft Word'deki şekle sol tıklamak yeni bir web tarayıcı penceresi açacaktır
// ve bizi "HRef" özelliğindeki köprüye götür.
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


