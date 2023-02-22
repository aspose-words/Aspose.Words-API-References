---
title: OfficeMath.GetMathRenderer
second_title: Aspose.Words for .NET API Referansı
description: OfficeMath yöntem. Bu denklemi bir görüntüye dönüştürmek için kullanılabilecek bir nesne oluşturur ve döndürür.
type: docs
weight: 80
url: /tr/net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

Bu denklemi bir görüntüye dönüştürmek için kullanılabilecek bir nesne oluşturur ve döndürür.

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### Geri dönüş değeri

Bu denklem için oluşturucu nesnesi.

### Notlar

Bu yöntem sadece[`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/)yapıcı ve bu nesneyi parametre olarak iletir.

### Örnekler

Yerel dosya sisteminde bir Office Math nesnesinin bir görüntü dosyasına nasıl dönüştürüleceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Düğüm oluşturucunun değiştirilecek "Kaydet" yöntemine geçmek için bir "ImageSaveOptions" nesnesi oluşturun
// OfficeMath düğümünü bir görüntüye nasıl dönüştürdüğü.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// Nesneyi orijinal boyutunun beş katına çıkarmak için "Scale" özelliğini 5'e ayarlayın.
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### Ayrıca bakınız

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* ad alanı [Aspose.Words.Math](../../officemath/)
* toplantı [Aspose.Words](../../../)


