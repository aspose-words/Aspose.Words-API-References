---
title: MetafileRenderingOptions.UseEmfEmbeddedToWmf
linktitle: UseEmfEmbeddedToWmf
articleTitle: UseEmfEmbeddedToWmf
second_title: .NET için Aspose.Words
description: UseEmfEmbeddedToWmf özelliğinin WMF meta dosyası oluşturmayı nasıl optimize ettiğini, grafik uygulamalarınızın performansını ve kalitesini nasıl artırdığını keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/
---
## MetafileRenderingOptions.UseEmfEmbeddedToWmf property

Gömülü EMF meta dosyalarına sahip WMF meta dosyalarının nasıl işleneceğini belirleyen bir değer alır veya ayarlar.

```csharp
public bool UseEmfEmbeddedToWmf { get; set; }
```

## Notlar

WMF meta dosyaları gömülü EMF verileri içerebilir. MS Word çoğu durumda gömülü EMF verilerini kullanır. GDI+ her zaman WMF verilerini kullanır.

Bu değer olarak ayarlandığında`doğru`, Aspose.Words, oluşturma sırasında gömülü EMF verilerini kullanır.

Bu değer olarak ayarlandığında`YANLIŞ`, Aspose.Words, oluşturma sırasında WMF verilerini kullanır.

Bu seçenek yalnızca meta dosyası vektör grafikleri olarak işlendiğinde kullanılır. Meta dosyası bitmap olarak rendered olduğunda, WMF verileri her zaman kullanılır.

Varsayılan değer:`doğru`.

## Örnekler

PDF'ye kaydederken Gelişmiş Windows Meta Dosyası ile ilgili işleme seçeneklerinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.Emf" olarak ayarlayın
// EMF+ ikili meta dosyasının yalnızca EMF kısmını işlemek için.
// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.EmfPlus" olarak ayarlayın
// EMF+ ikili meta dosyasının EMF+ kısmını işlemek için.
// "EmfPlusDualRenderingMode" özelliğini "EmfPlusDualRenderingMode.EmfPlusWithFallback" olarak ayarlayın
// EMF+ kayıtlarının tümü destekleniyorsa, EMF+ ikili meta dosyasının EMF+ kısmını işlemek için.
// Aksi halde Aspose.Words EMF kısmını işleyecektir.
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// Gömülü EMF verilerini işlemek için "UseEmfEmbeddedToWmf" özelliğini "true" olarak ayarlayın
// vektörel grafikler olarak işlenebilecek meta dosyaları için.
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### Ayrıca bakınız

* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
