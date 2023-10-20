---
title: PdfSaveOptions.ZoomBehavior
linktitle: ZoomBehavior
articleTitle: ZoomBehavior
second_title: Aspose.Words for .NET
description: PdfSaveOptions ZoomBehavior mülk. Bir belge PDF görüntüleyiciyle açıldığında ne tür yakınlaştırmanın uygulanması gerektiğini belirleyen bir değer alır veya ayarlar C#'da.
type: docs
weight: 320
url: /tr/net/aspose.words.saving/pdfsaveoptions/zoombehavior/
---
## PdfSaveOptions.ZoomBehavior property

Bir belge PDF görüntüleyiciyle açıldığında ne tür yakınlaştırmanın uygulanması gerektiğini belirleyen bir değer alır veya ayarlar.

```csharp
public PdfZoomBehavior ZoomBehavior { get; set; }
```

## Notlar

Varsayılan değer:None , yani hiçbir uyum uygulanmadı.

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

* enum [PdfZoomBehavior](../../pdfzoombehavior/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
