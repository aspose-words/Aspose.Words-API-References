---
title: MetafileRenderingOptions.EmfPlusDualRenderingMode
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: .NET için Aspose.Words
description: EmfPlusDualRenderingMode özelliğinin EMF Dual meta dosyası oluşturmayı nasıl geliştirdiğini keşfedin. Grafiklerinizi bugün esnek oluşturma seçenekleriyle optimize edin!
type: docs
weight: 20
url: /tr/net/aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/
---
## MetafileRenderingOptions.EmfPlusDualRenderingMode property

EMF+ Dual meta dosyalarının nasıl işleneceğini belirleyen bir değer alır veya ayarlar.

```csharp
public EmfPlusDualRenderingMode EmfPlusDualRenderingMode { get; set; }
```

## Notlar

EMF+ Dual meta dosyaları hem EMF+ hem de EMF parçalarını içerir. MS Word ve GDI+ her zaman EMF+ parçasını işler. Aspose.Words şu anda tüm EMF+ kayıtlarını tam olarak desteklemiyor ve bazı durumlarda EMF parçasının işlenmesi sonucu EMF+ parçasının işlenmesinden daha iyi görünüyor.

Bu seçenek yalnızca meta dosyası vektör grafikleri olarak işlendiğinde kullanılır. Meta dosyası bitmap'e rendered yapıldığında, EMF+ kısmı her zaman kullanılır.

Varsayılan değer:EmfPlusWithFallback.

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

* enum [EmfPlusDualRenderingMode](../../emfplusdualrenderingmode/)
* class [MetafileRenderingOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
