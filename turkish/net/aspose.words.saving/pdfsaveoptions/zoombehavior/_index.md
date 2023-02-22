---
title: PdfSaveOptions.ZoomBehavior
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. Bir belge PDF görüntüleyici ile açıldığında ne tür yakınlaştırmanın uygulanması gerektiğini belirleyen bir değer alır veya ayarlar.
type: docs
weight: 290
url: /tr/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

Bir belge PDF görüntüleyici ile açıldığında ne tür yakınlaştırmanın uygulanması gerektiğini belirleyen bir değer alır veya ayarlar.

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

### Notlar

Varsayılan değerNone , yani hiçbir uyum uygulanmadı.

### Örnekler

İşlenmiş bir PDF belgesini açarken okuyucunun uyguladığı varsayılan yakınlaştırmanın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
// Bir PDF okuyucusu almak için "ZoomBehavior" özelliğini "PdfZoomBehavior.ZoomFactor" olarak ayarlayın
// belgeyi onunla açtığımızda yüzde tabanlı bir yakınlaştırma faktörü uygularız.
// Yakınlaştırma faktörüne %25'lik bir değer vermek için "ZoomFactor" özelliğini "25" olarak ayarlayın.
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
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


