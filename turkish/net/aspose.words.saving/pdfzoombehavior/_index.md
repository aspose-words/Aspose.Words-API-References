---
title: Enum PdfZoomBehavior
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.PdfZoomBehavior Sıralama. PDF görüntüleyicide açıldığında PDF belgesine uygulanan yakınlaştırma türünü belirtir.
type: docs
weight: 5540
url: /tr/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

PDF görüntüleyicide açıldığında PDF belgesine uygulanan yakınlaştırma türünü belirtir.

```csharp
public enum PdfZoomBehavior
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Belgenin nasıl görüntüleneceği PDF görüntüleyiciye bırakılmıştır. Görüntüleyici genellikle belgeyi sayfa genişliğine sığacak şekilde görüntüler. |
| ZoomFactor | `1` | Belirtilen yakınlaştırma faktörünü kullanarak sayfayı görüntüler. |
| FitPage | `2` | Sayfayı tamamen görünür olacak şekilde görüntüler. |
| FitWidth | `3` | Sayfanın genişliğine sığdırır. |
| FitHeight | `4` | Sayfanın yüksekliğine sığdırır. |
| FitBox | `5` | Sınırlayıcı kutuya sığar (sayfadaki tüm görünür öğeleri içeren dikdörtgen). |

### Örnekler

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


