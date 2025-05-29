---
title: PdfZoomBehavior Enum
linktitle: PdfZoomBehavior
articleTitle: PdfZoomBehavior
second_title: .NET için Aspose.Words
description: Özelleştirilebilir PDF yakınlaştırma ayarları için Aspose.Words.PdfZoomBehavior enum'unu keşfedin. PDF belgelerinde özelleştirilmiş görüntüleme seçenekleriyle kullanıcı deneyimini geliştirin.
type: docs
weight: 6340
url: /tr/net/aspose.words.saving/pdfzoombehavior/
---
## PdfZoomBehavior enumeration

Bir PDF görüntüleyicide açıldığında PDF belgesine uygulanan yakınlaştırma türünü belirtir.

```csharp
public enum PdfZoomBehavior
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Belgenin nasıl görüntüleneceği PDF görüntüleyicisine bırakılmıştır. Genellikle görüntüleyici belgeyi sayfa genişliğine uyacak şekilde görüntüler. |
| ZoomFactor | `1` | Sayfayı belirtilen yakınlaştırma faktörünü kullanarak görüntüler. |
| FitPage | `2` | Sayfayı tamamen görünür şekilde görüntüler. |
| FitWidth | `3` | Sayfanın genişliğine uyar. |
| FitHeight | `4` | Sayfanın yüksekliğine uyar. |
| FitBox | `5` | Sınırlayıcı kutuya (sayfadaki tüm görünür öğeleri içeren dikdörtgen) uyar. |

## Örnekler

İşlenmiş bir PDF belgesini açarken okuyucunun uygulayacağı varsayılan yakınlaştırmanın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
// PDF okuyucusunun "ZoomBehavior" özelliğini "PdfZoomBehavior.ZoomFactor" olarak ayarlaması için
// belgeyi açtığımızda yüzdeye dayalı bir yakınlaştırma faktörü uygula.
// Yakınlaştırma faktörüne %25 değerini vermek için "ZoomFactor" özelliğini "25" olarak ayarlayın.
PdfSaveOptions options = new PdfSaveOptions
{
    ZoomBehavior = PdfZoomBehavior.ZoomFactor,
    ZoomFactor = 25
};

// Bu belgeyi Adobe Acrobat gibi bir okuyucu kullanarak açtığımızda, belgenin gerçek boyutunun 1/4'ü oranında ölçeklendiğini göreceğiz.
doc.Save(ArtifactsDir + "PdfSaveOptions.ZoomBehaviour.pdf", options);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
