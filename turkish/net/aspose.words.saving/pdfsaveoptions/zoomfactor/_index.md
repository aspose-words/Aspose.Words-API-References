---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: Aspose.Words for .NET
description: PdfSaveOptions ZoomFactor mülk. Bir belge için yakınlaştırma faktörünü belirleyen değeri yüzde cinsinden alır veya ayarlar C#'da.
type: docs
weight: 330
url: /tr/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

Bir belge için yakınlaştırma faktörünü belirleyen değeri (yüzde cinsinden) alır veya ayarlar.

```csharp
public int ZoomFactor { get; set; }
```

## Notlar

Bu değer yalnızca şu durumlarda kullanılır:[`ZoomBehavior`](../zoombehavior/) ayarlandıZoomFactor .

## Örnekler

Okuyucunun işlenmiş bir PDF belgesini açarken uyguladığı varsayılan yakınlaştırmanın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
// Bir PDF okuyucunun çalışmasını sağlamak için "ZoomBehavior" özelliğini "PdfZoomBehavior.ZoomFactor" olarak ayarlayın
// belgeyi bununla açtığımızda yüzdeye dayalı bir yakınlaştırma faktörü uygulayın.
// Yakınlaştırma faktörüne %25 değerini vermek için "ZoomFactor" özelliğini "25" olarak ayarlayın.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Bu belgeyi Adobe Acrobat gibi bir okuyucu kullanarak açtığımızda belgenin gerçek boyutunun 1/4'ü oranında ölçeklenmiş olduğunu göreceğiz.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
