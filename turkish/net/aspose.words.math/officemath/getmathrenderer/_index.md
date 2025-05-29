---
title: OfficeMath.GetMathRenderer
linktitle: GetMathRenderer
articleTitle: GetMathRenderer
second_title: .NET için Aspose.Words
description: Denklemleri zahmetsizce görsellere dönüştürmek ve belgelerinizi net, profesyonel görsellerle zenginleştirmek için OfficeMath'in GetMathRenderer yöntemini keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

Bu denklemi bir görüntüye dönüştürmek için kullanılabilecek bir nesne oluşturur ve döndürür.

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### Geri dönüş değeri

Bu denklemin işleyici nesnesi.

## Notlar

Bu yöntem yalnızca şunu çağırır:[`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/) constructor'ı kullanın ve bu nesneyi parametre olarak pass olarak geçirin.

## Örnekler

Office Math nesnesinin yerel dosya sisteminde bir görüntü dosyasına nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Düğüm oluşturucusunun "Kaydet" yöntemine geçirilecek ve değiştirilecek bir "ImageSaveOptions" nesnesi oluşturun
// OfficeMath düğümünü bir görüntüye nasıl dönüştürdüğü.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Nesneyi orijinal boyutunun beş katına çıkarmak için "Ölçek" özelliğini 5 olarak ayarlayın.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Ayrıca bakınız

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* ad alanı [Aspose.Words.Math](../../../aspose.words.math/)
* toplantı [Aspose.Words](../../../)
