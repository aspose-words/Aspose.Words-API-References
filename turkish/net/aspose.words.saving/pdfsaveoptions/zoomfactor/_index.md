---
title: PdfSaveOptions.ZoomFactor
linktitle: ZoomFactor
articleTitle: ZoomFactor
second_title: .NET için Aspose.Words
description: Belge yakınlaştırma düzeylerini yüzde olarak kolayca ayarlamak ve PDF görüntüleme deneyiminizi geliştirmek için PdfSaveOptions'ın ZoomFactor özelliğini keşfedin.
type: docs
weight: 360
url: /tr/net/aspose.words.saving/pdfsaveoptions/zoomfactor/
---
## PdfSaveOptions.ZoomFactor property

Bir belge için yakınlaştırma faktörünü (yüzde olarak) belirleyen bir değer alır veya ayarlar.

```csharp
public int ZoomFactor { get; set; }
```

## Notlar

Bu değer yalnızca şu durumlarda kullanılır:[`ZoomBehavior`](../zoombehavior/) ayarlandıZoomFactor .

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

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
