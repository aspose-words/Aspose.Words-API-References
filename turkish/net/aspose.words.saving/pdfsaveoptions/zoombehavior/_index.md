---
title: PdfSaveOptions.ZoomBehavior
linktitle: ZoomBehavior
articleTitle: ZoomBehavior
second_title: .NET için Aspose.Words
description: PdfSaveOptions ZoomBehavior'ı keşfedin, PDF görüntüleyicilerde optimum görüntüleme için yakınlaştırma ayarlarını kontrol edin. Özelleştirilmiş belge görüntülemeyle kullanıcı deneyimini geliştirin!
type: docs
weight: 350
url: /tr/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

Bir belge PDF görüntüleyicisiyle açıldığında hangi tür yakınlaştırmanın uygulanacağını belirleyen bir değer alır veya ayarlar.

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

## Notlar

Varsayılan değer:None , yani hiçbir uyum uygulanmadı.

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

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
