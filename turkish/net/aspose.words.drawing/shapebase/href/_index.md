---
title: ShapeBase.HRef
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Bir şekil için tam köprü adresini alır veya ayarlar.
type: docs
weight: 220
url: /tr/net/aspose.words.drawing/shapebase/href/
---
## ShapeBase.HRef property

Bir şekil için tam köprü adresini alır veya ayarlar.

```csharp
public string HRef { get; set; }
```

### Notlar

Varsayılan değer boş bir dizedir.

Aşağıda bu özellik için geçerli değer örnekleri verilmiştir:

Tam URI:`https://www.aspose.com/`.

Tam dosya adı:`C:\\Belgelerim\\SatışRaporu.doc`.

Göreli URI:`../../../resource.txt`

Göreli dosya adı:`..\\Belgelerim\\Satış Raporu.doc`.

Başka bir belgede yer imi:`https://www.aspose.com/Products/Default.aspx#Suites`

Bu belgedeki yer imi:`#BookmakName`.

### Örnekler

Görüntü içeren ve aynı zamanda bir köprü olan bir şeklin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Microsoft Word'de şekle Ctrl + sol tıklamak yeni bir web tarayıcı penceresi açacaktır
// ve bizi "HRef" özelliğindeki köprüye götürün.
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


