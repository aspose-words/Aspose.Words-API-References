---
title: DocumentBase.BackgroundShape
second_title: Aspose.Words for .NET API Referansı
description: DocumentBase mülk. Belgenin arka plan şeklini alır veya ayarlar. Olabilirhükümsüz .
type: docs
weight: 10
url: /tr/net/aspose.words/documentbase/backgroundshape/
---
## DocumentBase.BackgroundShape property

Belgenin arka plan şeklini alır veya ayarlar. Olabilir`hükümsüz` .

```csharp
public Shape BackgroundShape { get; set; }
```

### Notlar

Microsoft Word yalnızca kendine ait bir şekle izin verir[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) özellik equal -Rectangle bir belge için arka plan şekli olarak kullanılacak.

Microsoft Word yalnızca arka plan şeklinin dolgu özelliklerini destekler. Diğer tüm özellikler yoksayılır.

Bu özelliğin null olmayan bir değere ayarlanması aynı zamanda[`DisplayBackgroundShape`](../../../aspose.words.settings/viewoptions/displaybackgroundshape/) ile`doğru`.

### Örnekler

Bir belgenin her sayfası için arka plan şeklinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

Assert.IsNull(doc.BackgroundShape);

// Arka plan olarak kullanabileceğimiz tek şekil türü dikdörtgendir.
Shape shapeRectangle = new Shape(doc, ShapeType.Rectangle);

// Bu şekli sayfa arka planı olarak kullanmanın iki yolu vardır.
// 1 - Düz bir renk:
shapeRectangle.FillColor = System.Drawing.Color.LightBlue;
doc.BackgroundShape = shapeRectangle;

doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.FlatColor.docx");

// 2 - Bir resim:
shapeRectangle = new Shape(doc, ShapeType.Rectangle);
shapeRectangle.ImageData.SetImage(ImageDir + "Transparent background logo.png");

// Filigran olarak daha uygun hale getirmek için görüntünün görünümünü ayarlayın.
shapeRectangle.ImageData.Contrast = 0.2;
shapeRectangle.ImageData.Brightness = 0.7;

doc.BackgroundShape = shapeRectangle;

Assert.IsTrue(doc.BackgroundShape.HasImage);

Aspose.Words.Saving.PdfSaveOptions saveOptions = new Aspose.Words.Saving.PdfSaveOptions
{
    CacheBackgroundGraphics = false
};

// Microsoft Word, arka plan olarak resim içeren şekilleri desteklemez,
// ancak bu arka planları hala .pdf gibi diğer kaydetme formatlarında görebiliriz.
doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

### Ayrıca bakınız

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBase](../)
* ad alanı [Aspose.Words](../../documentbase/)
* toplantı [Aspose.Words](../../../)


